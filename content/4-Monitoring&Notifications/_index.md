---
title : "Giám sát & Thông báo"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

1. Vào **AWS Console** → **AWS Config**
 + Nhấn “Get started” nếu chưa cấu hình
 + Chọn:
      + **Resources to record** → **Record all resources supported in this region**
      + **Amazon S3 bucket** → tạo mới hoặc chọn sẵn (dùng để lưu log)
      + **IAM Role** → cho phép tạo mới role **AWSConfigRole**
 + Nhấn **Confirm**

2. Trong **AWS Config**, vào tab **Rules**
 + Click **Add rule**

![Config](/images/1.intro/Rule.png)

 + Tại trang **Specify rule type**
 + Tìm rule có tên: **acm-certificate-expiration-check**
 + Click **Next**

![Config](/images/1.intro/AddRule.png)

 + Cấu hình:
     + **Scope of changes**: **All changes**
     + **Maximum days before expiration**: 14
 + Click **Next**

![Config](/images/1.intro/ConfigRule.png)

 + Click **Save**

 + Tiếp theo, tạo **Simple Notification Service (SNS)** để nhận thông báo
 + Tại giao diện trang chủ của **SNS**, nhập **tên topic**: **SSLExpirationAlerts**
 + Click **Next step**

![SNS](/images/1.intro/SNS.png)

 + Tại trang **Create topic**
 + Chọn **Standard**
 + Click **Create topic**

![SNS](/images/1.intro/CreateSNS.png)

 + Tại trang được chuyển tới, click **Create subscription**
 + Tại trang **Details**
 + Tại mục **Protocol** chọn **Email**
 + Tại mục **Endpoint** nhập **Email của bạn**
 + Click **Create subscription**

![SNS](/images/1.intro/Details.png)

 + Bạn sẽ nhận được một **email xác nhận** → **Check mail & Confirm**