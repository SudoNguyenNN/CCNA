![image](https://user-images.githubusercontent.com/50360416/195252644-8af15f39-c80b-45a3-b595-4735bb2e781c.png)

*Kết Quả*

![image](https://user-images.githubusercontent.com/50360416/195262719-7696701e-3a8f-43d9-acbb-2fdb15b9acaa.png)


Cấu hình :

Router rip				bật tính năng rip 

	Version 2			bật tính năng version 2     /22 ( classless /  classful A , b ,C )
  
	No auto-summary		tắt tính năng tổng hợp tuyến đường đi
  
	Passive-interface g0/1		thụ động cổng g0/1 tăng hiệu năng/ tăng bảo mật
  
	Net 192.168.1.0
  
	Net 192.168.2.0	
  
	Net 192.168.10.0
  
	Ex 
  
  
Nếu là router Gate thì  có 1 câu lệnh nữa

	Default-information originate 		
  
	Def ori
  
ở đây có defaut route   1/  không mô tả chi tiết default đi như nào 

			2/ kể cả ko có default route thì vẫn cứ giới thiệu bình thường
      
      
      
### Note: Rip có AD=120 và Metric của RIP bằng số nexthop ( route để đến đích)


=============================================================================================

### BT Tổng hợp :

- Vlan
- Trunking
- Routing: RIP

![image](https://user-images.githubusercontent.com/50360416/195269309-195e38cf-967f-409e-9da3-4deb38cbdf9c.png)

