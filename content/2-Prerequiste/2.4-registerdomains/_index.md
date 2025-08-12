---
title : "Đăng ký tên miền với Route 53"
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

1. Truy cập **Giao diện dịch vụ Route 53**
  + Click **Registered domains**.
  + Click **Register domains**.
  
![Route53](/images/1.intro/Route53.png)

1. Tại trang **Register domains**.
 + Tại mục  **Check availability for a domain** nhập tên domains mà bạn muốn.
 + Click **Search**.
 + Tại **Search result**, nếu domains bạn nhập chưa có ai đăng ký thì sẽ hiển thị **Exact match** và bạn có thể tham khảo giá domains ở bên cạnh, hoặc xem các đề xuất ở bên dưới.
 + Sau khi chọn, click **Select**
 
![Route53](/images/1.intro/RegisterDomain.png)

 + Click **Proceed to checkout**

![Route53](/images/1.intro/SelectDomains.png)

 + Tại mục **Pricing**, kiểm tra lại tên domain + giá, click **Next**
 + Tại mục **Contact information**, nhập thông tin liên lạc của bản thân và click **Next**
 + Tại mục **Review and submit**, kiểm tra kĩ lại các thông tin quan trọng

![Route53](/images/1.intro/BeforeSubmit.png)

 + Click **Submit**
 + Sau khi Submit, khoảng 10~15phút sau Amazon sẽ gửi cho bạn email xác nhận đăng kí domains, kiểu như hình dưới đây.

![Route53](/images/1.intro/VerifyDomains.png)

 + Vậy là bạn đã đăng ký domain thành công với Route 53.

1. Tiếp theo, tạo **Hosted Zone**
 + Chọn **Hosted Zone** trong giao diện dịch vụ **Route 53**
 + Click **Create Hosted Zone**

![Route53](/images/1.intro/HostedZone.png)

 + Tại trang **Create hosted zone**, tại mục **Domain name** nhập tên domain của bạn.
 + Click **Create hosted zone**

![Route53](/images/1.intro/CreateHostedZone.png)

Hoàn thành các bước chuẩn bị với **Route 53**