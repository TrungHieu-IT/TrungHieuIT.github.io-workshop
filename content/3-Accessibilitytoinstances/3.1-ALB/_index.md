---
title : "Tạo Application Load Balancer (ALB) + Target group"
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---

1. Go to [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home).
  + Click **Load Balancers**.
  + Click **Create load balancer**.

![ALB](/images/1.intro/ALB.png)

  + Click to Create **Application load balancer**.
  + Click **Save**.

1. Tại trang **Create Application Load Balancer**
  + Tại mục **Load balancer name** nhập **Workshop**
  + Tại mục **Scheme** chọn **Internet-facing**
  + Tại mục **Load balancer IP address type** chọn **IPv4**

![ALB](/images/1.intro/CreateALBScr.png)

2. Trong phần **Network mapping**
  + Tại mục **VPC** chọn VPC vừa tạo tại trong phần chuẩn bị
  + Tại mục **Availability Zones and subnets** chọn vùng của bạn và chọn 2 Subnet đã tạo trong phần chuẩn bị

![ALB](/images/1.intro/CreateALBScr2.png)

3. Trong phần **Security groups** chọn **default**

![ALB](/images/1.intro/SGDefault.png)

4. Trong phần **Listeners and routing**
  + Click **Create target group**
  
![ALB](/images/1.intro/ClTarget.png)

1. Tại trang **Specify group details**
  + Tại mục **Choose a target type** chọn **Instance**
  + Tại mục **Target group name** nhập **Workshop**
  + Tại mục **IP address type** chọn **IPv4**
  + Tại mục **VPC** chọn VPC đã tạo trong phần chuẩn bị.
  + Tại mục **Protocol version** chọn **HTTP1**
  + Trong phần **Health checks**, tại mục **Health check protocol** chọn **HTTP**
  + Click **Next**

2. Tại trang **Register targets**
  + Trong phần **Available instances** chọn Instance đã tạo trong phần chuẩn bị.
  + Click **Create target group**

3. Tiếp tục trong phần **Listeners and routing**
  + Tại mục **Listener HTTP:80** chọn **target group** là target group mới tạo
  + Click **Add listener**
  + Chọn **Protocol** là **HTTPS**
  + chọn **target group** là target group mới tạo

![ALB](/images/1.intro/Listener.png)