---
title : "Gán certificate vào ALB (HTTPS listener)"
weight : 4
chapter : false
pre : " <b> 3.4. </b> "
---
1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
 + Click **Load balancer**
 + Chọn **Load balancer** đã tạo từ trước.

![Alb](/images/1.intro/ChooseAlb.png)

2. Trong trang được chuyển tới
 + Chọn tab **Listeners and rules**
 + Click **HTTPS:443**

![Alb](/images/1.intro/HTTPS.png)

 + Chọn tab **Certificates**
 + Click **Add certificate**

![Alb](/images/1.intro/AddCert.png)

 + Chọn hết các **Certificate**
 + Click **Include as pending below**

![Alb](/images/1.intro/IncludeAs.png)

 + Click **Add pending certificates**

