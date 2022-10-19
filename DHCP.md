![image](https://user-images.githubusercontent.com/50360416/196613060-fc18796f-5623-44a8-a45e-6079756d06f7.png)

DHCP(config)#ip dhcp excluded-address 192.168.10.1 192.168.10.10   : Loại bỏ dải địa chỉ IP này ra khỏi quá trình cấp DHCP ( cũng có thể loại bỏ từng địa chỉ )

DHCP(config)#ip dhcp pool IT  : Tạo tên cấp DHCP

DHCP(dhcp-config)#network 192.168.10.0 255.255.255.0  : Tạo dải cấp địa chỉ IP tự động ( sẽ loại dải địa chỉ IP đã *excluded* )

DHCP(dhcp-config)#dns 8.8.8.8  : địa chỉ IP DNS

DHCP(dhcp-config)#default-router 192.168.10.1  : Địa chỉ IP Default Gateway


===================================

ip helper-add 192.168.50.2   : Xin cấp địa chỉ IP từ cổng có địa chỉ IP 192.168.50.2



Laps: 

![image](https://user-images.githubusercontent.com/50360416/196653227-684e417d-4353-4e64-894b-ad38d85cc747.png)


Xin cấp địa chỉ IP

![image](https://user-images.githubusercontent.com/50360416/196653401-715c056d-5052-4786-8a16-0dbe2216b716.png)


Ping 

![image](https://user-images.githubusercontent.com/50360416/196653539-ab454ec6-9470-45bc-827a-5c1ac9099dff.png)





Câu lệnh trên Swich Core * tham khảo*

Core sw brand

Ena

Conf t

Host Brand

Ip routing

exit

Int g1/0/1

No sw

No sh

Ip add 192.168.70.2 255.255.255.0

Ip route 0.0.0.0 0.0.0.0 192.168.70.1

Exit

Int g1/0/2

No sw

No sh

Ip add 192.168.50.1 255.255.255.0

Ip route 0.0.0.0 0.0.0.0 192.168.50.2

Exit

Int ran g1/0/3-6

Channel-gr 2 mode ac

Ex

Int port 2

Sh

Sw tr en do

Sw mo tr

No sh

Ex

Vl 30

Vl 40

Ex

Int vl 30

No sh

Ip add 192.168.30.1 255.255.255.0

ip helper-add 192.168.50.2

Ex

Int vl 40

No sh

Ip add 192.168.40.1 255.255.255.0

ip helper-add 192.168.50.2

Exit

Router rip

Ver 2

No au

Net 192.168.30.0

Net 192.168.40.0

Net 192.168.50.0

Net 192.168.70.0

Exit




