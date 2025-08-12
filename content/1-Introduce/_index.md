---
title : "Giới thiệu"
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**AWS Certificate Manager (ACM)** là dịch vụ của **Amazon Web Services** giúp bạn cung cấp, quản lý và triển khai chứng chỉ số **SSL/TLS** một cách miễn phí và tự động.

Chứng chỉ **SSL/TLS** được dùng để mã hóa kết nối giữa người dùng và ứng dụng (HTTPS), bảo vệ dữ liệu khỏi bị nghe lén hoặc giả mạo.

**Route 53**

Amazon Route 53 là dịch vụ DNS (Domain Name System) được quản lý bởi AWS, cung cấp khả năng phân giải tên miền một cách nhanh chóng, đáng tin cậy và linh hoạt. Route 53 cho phép người dùng định tuyến lưu lượng truy cập đến các máy chủ, ứng dụng hoặc tài nguyên AWS dựa trên nhiều chính sách như địa lý, trọng số và trạng thái sức khỏe của endpoint. Ngoài ra, dịch vụ còn hỗ trợ mua và quản lý tên miền, giúp doanh nghiệp xây dựng hạ tầng mạng toàn cầu với hiệu suất cao và độ sẵn sàng tối ưu.

**Mục đích chính**
  - Tạo chứng chỉ SSL/TLS mà không cần phải mua từ nhà cung cấp bên thứ ba.
  - Tự động gia hạn chứng chỉ trước khi hết hạn (tránh downtime).
  - Triển khai nhanh chứng chỉ tới các dịch vụ AWS như:
     * Elastic Load Balancer (ELB / ALB / NLB)
     * Amazon CloudFront
     * Amazon API Gateway
     * AWS App Runner

**Ưu điểm nổi bật**.
  - Miễn phí chứng chỉ công khai do ACM cấp.
  - Tự động gia hạn — không cần thao tác thủ công.
  - Tích hợp sẵn với dịch vụ AWS — gắn chứng chỉ chỉ với vài cú click.
  - Hỗ trợ cả chứng chỉ công khai và chứng chỉ nội bộ (private CA).
  - Bảo mật cao, đáp ứng tiêu chuẩn ngành (RSA 2048-bit, ECC).

**Sơ đồ kiến trúc**

![Sodo](/Workshop/static/images/1.intro/Sodo1.png)
