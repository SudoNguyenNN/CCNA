## NAT

**NAT** hay **Network Address Translation** giúp địa chỉ mạng cục bộ (Private) truy cập đến mạng công cộng (Internet).

Config:

![image](https://github.com/SudoNguyenNN/CCNA/assets/50360416/8586b6fe-087d-4fb0-89fa-ecb12448f063)

**R-Local**

Router(config)#int g0/1

Router(config-if)#ip nat in

Router(config-if)#ip nat inside

Router(config-if)#int g0/0

Router(config-if)#ip nat ou

Router(config-if)#ip nat outside 

Router(config)#ip route 0.0.0.0 0.0.0.0 7.7.7.1

Router(config)#access-list 1 permit any 

Router(config)#ip nat inside source list 1 interface g0/0

**R-Google**

Router(config-if)#int g0/1

Router(config-if)#ip nat inside

Router(config)#int g0/0

Router(config-if)#ip nat outside 

Router(config)#ip route 0.0.0.0 0.0.0.0 8.8.8.1

Router(config)#ip nat inside source static tcp 192.168.10.10 80 8.8.8.8 80

Router(config)#ip nat inside source static tcp 192.168.10.10 443 8.8.8.8 443

**Kết quả**

PC: 192.168.20.10 truy cập được web của Server: 192.168.10.10 thông qua ip public 8.8.8.8

![image](https://github.com/SudoNguyenNN/CCNA/assets/50360416/a60915d6-f1af-4b9c-8768-728b4428c68e)
