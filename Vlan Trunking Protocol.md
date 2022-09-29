##Vlan Trunk Protocol : là giao thức hoạt động ở tầng liên kết dữ liệu trong mô hình OSI. VTP giúp cho việc cấu hình Vlan luôn được đồng nhất khi thêm, xóa, sửa thông tin về Vlan trong hệ thống.
## Cấu hình: 
![image](https://user-images.githubusercontent.com/50360416/192953660-9a4a2e41-b6c5-44c6-a590-d53cbd8e586b.png)

- SW_Core:
- 
SW_Core(config)#vtp mode server

SW_Core(config)#vtp version 2

SW_Core(config)#vtp domain nguyen.vn

SW_Core(config)#vtp password 123

SW_Core(config)#exit


SW_Core(config)#interface fastEthernet 0/1

SW_Core(config-if)#switchport mode trunk

SW_Core(config-if)#exit 

SW_Core(config)#interface fastEthernet 0/2

SW_Core(config-if)#switchport mode  trunk


### Note: Một số dòng switch không cần câu lệnh này sau câu lệnh mode trunk : switchport trunk encapsulation dots1q


- SW_Client:
- 
Switch(config)#vtp mode client 

Switch(config)#vtp domain nguyen.vn

Switch(config)#vtp password 123

Switch(config)#vtp version 2


SW_Client2(config)#interface fastEthernet 0/3

SW_Client2(config-if)#switchport mode access 

SW_Client2(config-if)#switchport access vlan 10


## Note: Cần cấu hình cổng nào cho Vlan nào thì cấu hình như bước trên

