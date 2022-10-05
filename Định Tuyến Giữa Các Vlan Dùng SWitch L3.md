![image](https://user-images.githubusercontent.com/50360416/193975272-25474615-e941-4884-a616-0577587c4adc.png)

Switch>en

Switch#

Switch#conf t

Switch(config)#hostname Core1

Core1(config)#vlan 10

Core1(config-vlan)#name IT

Core1(config-vlan)#vlan 20

Core1(config-vlan)#name Staff

Core1(config-vlan)#exit

Core1(config)#interface range gigabitEthernet 1/0/1-2

Core1(config-if-range)#no shutdown 

Core1(config-if-range)#ex

Core1(config)#interface gigabitEthernet 1/0/1

Core1(config-if)#switchport mode access 

Core1(config-if)#switchport access vlan 10

Core1(config-if)#ex

Core1(config)#interface gigabitEthernet 1/0/2

Core1(config-if)#switchport mode access 

Core1(config-if)#switchport access vlan 20

Core1(config-if)#ex

Core1(config)#interface vlan 10

Core1(config-if)#no shutdown

Core1(config-if)#ip address 192.168.10.1 255.255.255.0

Core1(config-if)#ex

Core1(config)#interface vlan 20

Core1(config-if)#no shutdown 

Core1(config-if)#ip address 192.168.20.1 255.255.255.0

Core1(config-if)#exit

Core1(config)#ip routing


### Note: Cần đặt Gateway cho PC trùng với Sub-Interface trên SW_Core thì pc-pc mới ping ok.


