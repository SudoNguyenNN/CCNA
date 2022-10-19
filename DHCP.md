![image](https://user-images.githubusercontent.com/50360416/196613060-fc18796f-5623-44a8-a45e-6079756d06f7.png)

DHCP(config)#ip dhcp excluded-address 192.168.10.1 192.168.10.10   : Loại bỏ dải địa chỉ IP này ra khỏi quá trình cấp DHCP ( cũng có thể loại bỏ từng địa chỉ )

DHCP(config)#ip dhcp pool IT  : Tạo tên cấp DHCP

DHCP(dhcp-config)#network 192.168.10.0 255.255.255.0  : Tạo dải cấp địa chỉ IP tự động ( sẽ loại dải địa chỉ IP đã *excluded* )

DHCP(dhcp-config)#dns 8.8.8.8  : địa chỉ IP DNS

DHCP(dhcp-config)#default-router 192.168.10.1  : Địa chỉ IP Default





