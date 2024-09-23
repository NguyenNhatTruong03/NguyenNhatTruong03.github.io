---
title : "Tạo phụ đề và dịch phụ đề cho video với AWS Transcribe và AWS Translate"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

### Tổng quan

 Khi xem một video bằng ngôn ngữ không quen thuộc hoặc không biết ngôn ngữ đó, bạn sẽ cần có phụ đề được dịch sang ngôn ngữ mà bạn hiểu. Đáp ứng nhu cầu này, chúng ta sẽ sử dụng kết hợp các dịch vụ mà AWS cung cấp để thực hiện việc tạo phụ đề và dịch phụ đề cho video. Sau cùng sẽ có được một video kèm theo phụ đề đã được dịch sang một ngôn ngữ quen thuộc giúp cho việc xem và hiểu nội dung của video dễ dàng hơn.
### Mục tiêu của Workshop hướng đến 
 From a video in English and without subtitles, after being processed to extract subtitles and translate subtitles into Vietnamese, at the end of the process, we will have a completed video in Vietnamese.
### Hạn chế của Worrkshop
 Tuy nhiên với Workshop này vẫn còn nhược điểm mà sau khi thực hiện Workshop sẽ thấy được là:
 - Quá trình upload video lên s3 chưa được tối ưu tốt, dẫn đến việc upload video diễn ra lâu và với video có thời lướng lớn thì quá trình này diễn ra lâu hơn nữa.
 - Nhận diện ngôn ngữ của video còn hạn chế, chỉ có video với ngôn ngữ tiếng anh.
 - Dịch phụ đề chỉ có từ tiếng anh sang tiếng việt.
### Hướng phát triển và cải tiến Workshop
 - Tối ưu hoá quá tringh upload video
 - Hỗ trợ phụ đề và dịch phụ đề đa ngôn ngữ.


![ConnectPrivate](./images/arc-log.png) 

#### Nội dung

 1. [Giới thiệu](1-introduce/)
 2. [Các bước chuẩn bị](2-Preparation/)
 3. [Cài đặt S3](3-Setup-S3/)
 4. [Upload video](4-Setup-Lambda-Upload-Video//)
 5. [Transcribe](5-Transcribe/)
 6. [Translate](6-Translate/)
 7. [Notify](7-Notify/)
 8. [Step Function](8-Step-Function/)
 9. [SNS](9-SNS/)
 10. [Call Step Function](10-Call-Step-Function/)
 11. [Chạy thử trang web](11-Test-website/)
 12. [Xoá tài nguyên](12-Clean-Up-Resources/)
