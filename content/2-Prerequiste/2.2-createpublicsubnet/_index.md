---
title : "Tạo 2 Public subnet và Internet Getway"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Public subnet

1. Click **Subnets**.
  + Click **Create subnet**.

![VPC](/images/1.intro/CreateSubnet.png)

1. Tại trang **Create subnet**.
  + Tại mục **VPC ID** click chọn **VPC-workshop**.
  + Tại mục **Subnet name** điền **workshop Public Subnet**.
  + Tại mục **Availability Zone** chọn Availability zone đầu tiên.
  + Tại mục **IPv4 CIRD block** điền **10.0.3.0/24**.

![VPC](/images/1.intro/CreateSubnetScreen.png)

3. Kéo xuống cuối trang , click **Create subnet**.

4. Click chọn **workshop Public Subnet**.
  + Click **Actions**.
  + Click **Edit subnet settings**.

![VPC](/images/1.intro/EditSubnet.png)

5. Click chọn **Enable auto-assign public IPv4 address**.
  + Click **Save**.

![VPC](/images/1.intro/SaveSettingSubnet.png)

Làm tương tự cho **Public subnet** thứ 2, nhưng tại **IPv4 CIRD block** điền **10.0.4.0/24**

![VPC](/images/1.intro/CreateSubnet2.png)

1. Click **Internet Gateways**.
  + Click **Create internet gateway**.
  
![VPC](/images/1.intro/IGW.png)

7. Tại trang **Create internet gateway**.
  + Tại mục **Name tag** điền **Workshop IGW**.
  + Click **Create internet gateway**.
  
![VPC](/images/1.intro/CreateIGW.png)

8. Sau khi tạo thành công, click **Actions**.
  + Click **Attach to VPC**.
 
![VPC](/images/1.intro/AttachToVPC.png)

9. Tại trang **Attach to VPC**.
  + Tại mục **Available VPCs** chọn **VPC-workshop**.
  + Click **Attach internet gateway**.
  + Kiểm tra quá trình attach thành công 

10. Tiếp theo chúng ta sẽ tạo một custom route table để gán vào **workshop Public Subnet**.
  + Click **Route Tables**.
  + Click **Create route table**.

![VPC](/images/1.intro/Route.png)

1.  Tại trang **Create route table**.
  + Tại mục **Name**, điền **Workshop Publicrtb**.
  + Tại mục **VPC**, chọn **VPC-workshop**.
  + Click **Create route table**.

2.  Sau khi tạo route table thành công.
  + Click **Edit routes**.
  
![VPC](/images/1.intro/EditRoute.png)

13. Tại trang **Edit routes**.
  + Click **Add route**.
  + Tại mục **Destination** điền 0.0.0.0/0
  + Tại mục **Target** chọn **Internet Gateway** sau đó chọn **Workshop IGW**.
  + Click **Save changes**.

![VPC](/images/1.intro/EditRoute1.png)

14. Click tab **Subnet associations**.
  + Click **Edit subnet associations** để tiến hành associate custom routable chúng ta vừa tạo vào **Lab Public Subnet**.


![VPC](/images/1.intro/EditAssociations.png)

15. Tại trang **Edit subnet associations**. 
  + Click chọn **workshop Public Subnet**.
  + Click **Save associations**.

![VPC](/images/1.intro/SaveAss.png)

16. Kiểm tra thông tin route table đã được associate với **Workshop Public Subnet** và thông tin route đi internet đã được trỏ đến Internet Gateway như hình dưới.


![VPC](/TrungHieuIT.github.io-workshop/static/images/1.intro/CheckAss.png)
