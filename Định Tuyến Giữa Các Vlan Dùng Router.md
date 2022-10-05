![image](https://user-images.githubusercontent.com/50360416/193966313-547eed23-6974-49c5-9f09-6e61e2b79080.png)

## S1:

 Ena
 
Conf t

Host S1

Vl 10

Name IT

Vl 20

Name HR

Ex


Int f0/3

Sw mo ac

Sw ac vl 10

Int f0/4

Sw mo ac

Sw ac vl 20

Ex

Int ran f0/1-2

Sw mo tr

Ex

## S2:

Ena
 
Conf t

Host S2

Vl 10

Name IT

Vl 20

Name HR

Ex


Int f0/3

Sw mo ac

Sw ac vl 10

Int f0/4

Sw mo ac

Sw ac vl 20

Ex

Int f0/2

Sw mo tr

Ex


## R1

Router: mo cong, sub int , dat ip

Ena 

Conf t

Host R1

Int g0/0

No sh

Ex

Int g0/0.10

En do 10

Ip add 192.168.10.1 255.255.255.0

Ex
Int g0/0.20

En do 20

Ip add 192.168.20.1 255.255.255.0

Ex

### Note: Phải đặt default gateway cho PC tương ứng với Sub interface đã chia cho từng vlan ở router



