---
title : "Tạo record A (Alias)"
weight : 3
chapter : false
pre : " <b> 3.3. </b> "
---

Trong phần này, chúng ta sẽ tạo **Record A (Alias)** cho domains

1. Truy cập **Giao diện dịch vụ Route 53**
 + Click **Hosted Zone**
 + Click vào domains đã tạo trong phần chuẩn bị

![ACM](/images/1.intro/Hosted.png)

 + Click **Create Record**
  
Tại trang **Create Record**
 + Tại mục **Record name** nhập domains mà bạn đã tạo
 + Tại mục **Record type** chọn **A**
 + Tại mục **Route traffic to** chọn lần lượt:
   + **Alias to Application and Classic Load Balancer**
   + Chọn **AZ** hiện tại của bạn
   + Chọn **Load balancer** đã tạo

![ACM](/images/1.intro/RecordA.png)

 + Click **Create records**