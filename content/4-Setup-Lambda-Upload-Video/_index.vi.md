---
title : "Cài đặt Lambda"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---


Để upload video vào s3, trong workshop này sẽ sử dụng Lambda để thực hiện upload video vào S3 bằng presigned URLs.

Presigned URL là URL mà bạn có thể cung cấp cho người dùng của mình để cấp quyền truy cập tạm thời vào một đối tượng S3 cụ thể. Sử dụng URL, người dùng có thể đọc và ghi đối tượng (hoặc cập nhật đối tượng hiện có). URL chứa các thông số cụ thể do ứng dụng mà bạn cài đặt. Presigned URL sử dụng ba tham số để giới hạn quyền truy cập cho người dùng:
- Bucket: Chứa các đối tượng - nơi đối tượng nằm trong đây.
- Key: Tên của đối tượng.
- Expires: thời hạn có hiệu lực của URL.

Sử dụng Lambda để tạo ra Presigned URL. Và ta sử dụng đơn luôn để tải nên giới hạn khích thức sẽ là *5GB*

### Nội dung:

  - [Tạo Lambda Function](./4.1-Create-Lambda/)

