---
title : "Tạo Public Linux EC2" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
  + Click **Instances**.
  + Click **Launch instances**.
  
![EC2](Workshop/static/images/1.intro/Instances.png)

2. Tại trang **Launch an instance**.
  + Nhập **Name**: **WorkshopEC2**
  + Trong phần **Quick Start** chọn **Amazon Linux**
  + Click **Select** để lựa chọn AMI **Amazon Linux 2023 kernel 6.1**.
  
![EC2](Workshop/static/images/1.intro/ChooseAMI.png)

1. Tiếp theo
 + Click chọn Instance type **t2.micro**.
 + Click **Create new Key pair**.
 
![EC2](Workshop/static/images/1.intro/TypeAndKeyPair.png)

1. Tại cửa sổ **Create key pair**
  + Tại mục **Key pair name** nhập: **MyWS**.
  + Tại mục **Key pair type** chọn **RSA**.
  + Tại mục **Private key file format** chọn **.pem**
  + Click **Create key pair**.

![EC2](Workshop/static/images/1.intro/KeyPair.png)

  + Trong phần **Key pair** chọn key vừa tạo

![EC2](Workshop/static/images/1.intro/SelectKey.png)

Trong phần **Network settings**.
  + Chọn **Allow HTTPS traffic from the internetp**.
  + Chọn **Allow HTTP traffic from the internet**.
  + Click **Lauch Instance**.

![EC2](Workshop/static/images/1.intro/Allow.png)

Trong tab **Instances** chọn Instance vừa tạo
  + Đợi cho **status check** chuyển thành **2/2 passed**
  + Click **Connect**

![EC2](Workshop/static/images/1.intro/22check.png)

  + Chuyển tới tab **Connect** thì tiếp tục click **Connect**
  + Sau đó sẽ hiện ra 1 tab như trong ảnh dưới

![EC2](Workshop/static/images/1.intro/ConnectEC2.png)

    yum update -y
    yum install -y httpd
    systemctl enable httpd
    systemctl start httpd
    echo "<h1>Hello HTTPS from EC2</h1>" > /var/www/html/index.html
  
  + Copy dòng lệnh trên và dán vào màn hình tương tác sẽ tạo ra 1 file hmtl đơn giản để chúng ta test



Tiếp theo chúng ta sẽ thực hiện tương tự để tạo 1 EC2 Instance Windows chạy trong Private subnet.
