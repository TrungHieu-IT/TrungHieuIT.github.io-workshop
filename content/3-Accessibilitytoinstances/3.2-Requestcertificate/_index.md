---
title : "Request certificate"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---

Truy cập [giao diện quản trị dịch vụ AWS Certificate Manager (ACM)](https://console.aws.amazon.com/acm/home)
+ Click **Request**

![ACM](/images/1.intro/Request.png)

+ Click **Next**

1. Tại trang **Request public certificate**
 + Tại mục **Fully qualified domain name** nhập domains mà bạn đã đăng ký với **Route 53**

![ACM](/images/1.intro/DomainsName.png)

 + Click **Request**

 + Trong trang bạn được chuyển tới, đợi cho **status** đổi thành **Issued**
 + Click copy **CNAME name**

![ACM](/images/1.intro/CopyCNAME.png)

1. Tới trang dịch vụ **Route 53**
 + Click **Hosted Zone**
 + Click vào domains đã tạo trong phần chuẩn bị

![ACM](/images/1.intro/Hosted.png)

 + Click **Create Record**

1. Tại trang **Create record**
 + Tại mục **Record name** nhập domains mà bạn đã tạo
 + Tại mục **Record type** chọn **CNAME**
 + Tại mục **Value** dán phần **CNAME name** đã copy từ trước vào

![ACM](/images/1.intro/CreateCNAME.png)

 + Click **Create Record**

