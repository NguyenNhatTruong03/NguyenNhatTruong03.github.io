---
title : "Cài đặt S3 cho trang web tĩnh"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1 </b> "
---

## Tạo Bucket S3

Truy cập đến bảng điều khiển S3 và tạo Bucket mới tên **`web-translate-ws-2024`**

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n1.png)

Chọn **ACLs enable** và tích **Object write để public các object trong bucket.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n2.png)

Bỏ tích **Block all public access*, tích **
I acknowledge that the current settings might result in this bucket and the objects within becoming public.** để có thể cho phép các nguồn khác có thể truy cập đến S3

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n.png)

**Create bucket**

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n3.png)

Chọn Bucket vừa tạo vào vào **Premissions**.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n4.png)

Đến **Bucket policy** để cấu hình policy Bucket.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n5.png)

Cấu hình policy cho bucket bằng tình năng **Policy generator**.

{{% notice note %}}
Trước khi chọn **Policy generator**, thì cần copy **Bucket ARN**
{{% /notice %}}

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n6.png)

Cấu hình để tạo policy cho bucket.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n7.png)

Kiểm tra xem đã chọn đủ các hành động có thể thực hiện với bucket này, đúng bucket arn.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n8.png)

Sau khi chọn **Generate Policy** sẽ được đoạn mã json policy và copy đoạn mã này.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n9.png)

Dán đoạn mã.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n10.png)

{{% notice note %}}
Ở cuối đừng dẫn trong **Resource** thêm /* để cho phép truy cập đến các object trong bucket.
{{% /notice %}}

**Save changes**

Upload file code trang web lên bucket, chọn upload và chọn file để upload lên và cuối cùng là bấm **Upload**.

Tải 2 file code:

- [index.html](https://drive.google.com/file/d/19ekeJsFYAZ-6qJIxMpHMbSsAyPruH26K/view?usp=sharing)

- [video-player.html](https://drive.google.com/file/d/1_S934h-snq5G-GxGSgEQrSX-eMHarYYn/view?usp=drive_link)

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n11.png)

Tạo static website hosting vào **Properties** sau đó đến **Static website hosting**.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n15.png)

Cấu hình static website hosting.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n13.png)

{{% notice note %}}
Phần **Index document** để tên file bạn muốn hiện thị gian diện đầu tiên, hay có thể như là trang chủ. Để đúng tên với file đã upload lên Bucket. **Error document** nếu bạn code file để hiện lỗi trang web thì có thể upload lên và để tên của file đó, ở đây do không có file hiện lỗi ở giao diện ên có thể để tên file như của  **Index document**.
{{% /notice %}}

**Save changes**

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n14.png)

Vậy đã xong và sẽ có đừng link đến trang web.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n16.png)