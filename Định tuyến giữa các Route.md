![image](https://user-images.githubusercontent.com/50360416/194514592-7b8aa877-f809-4deb-b36e-249b8f6c885e.png)

## R1:

Router(config)#interface gigabitEthernet 0/1

Router(config-if)#no shutdown 

Router(config-if)#ip address 192.168.10.1 255.255.255.0

Router(config-if)#ex

Router(config)#interface gigabitEthernet 0/0

Router(config-if)#no shutdown 

Router(config-if)#ip address 192.168.20.1 255.255.255.0

Router(config-if)#ex

Router(config)#ip route 0.0.0.0 0.0.0.0 192.168.20.2 

## GATE:

GATE(config)#interface gigabitEthernet 0/0

GATE(config-if)#no shutdown 

GATE(config-if)#ip address 192.168.20.2 255.255.255.0

GATE(config)#interface gigabitEthernet 0/1

GATE(config-if)#no shutdown

GATE(config-if)#ip address 192.168.30.2 255.255.255.0

GATE(config-if)#ex

GATE(config)#ip route 192.168.10.0 255.255.255.0 192.168.20.1

GATE(config)#ip route 192.168.40.0 255.255.255.0 192.168.30.3


## R2:

Router(config)#interface gigabitEthernet 0/0

Router(config-if)#no shutdown

Router(config-if)#ip address 192.168.30.3 255.255.255.0

Router(config-if)#ex

Router(config)#interface gigabitEthernet 0/1

Router(config-if)#no shutdown 

Router(config-if)#ip address 192.168.40.3 255.255.255.0

Router(config-if)#ex

Router(config)#ip route 0.0.0.0 0.0.0.0 192.168.30.2


### Note: Gateway PC trỏ về IP nối với SW














