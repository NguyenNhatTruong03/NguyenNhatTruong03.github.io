---
title : "Caption and translate video with AWS Transcribe and AWS Translate"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
### Overview

 When watching a video in a language that is unfamiliar or unknown to you, you will need subtitles translated into a language you understand. To meet this need, we will use a combination of AWS services to create and translate subtitles for the video. Ultimately, this will result in a video accompanied by subtitles translated into a familiar language, making it easier to watch and understand the content of the video.
### Target of the Workshop 
 From a video with English language and no subtitles, then after being processed to extract subtitles and translate subtitles into Vietnamese, the end of the process will be a video with complete Vietnamese subtitles.
### Limitations of Worrkshop
 However, this Workshop still has disadvantages that after doing the Workshop, you will see:
 - The process of uploading videos to S3 is not well optimized, leading to video uploading taking a long time and with videos of long duration, this process takes even longer.
 - The language recognition of the video is limited, only videos in English.
 - Subtitle translation is only from English to Vietnamese.
### Workshop Development and Improvement Directions
 - Optimize the video upload process.
 - Support subtitles and multilingual subtitle translation.

### Content
1. [Introduction](1-introduce/)
2. [Preparation steps](2-Preparation/)
3. [Setup S3](3-Setup-S3/)
4. [Upload video](4-Setup-Lambda-Upload-Video//)
5. [Transcribe](5-Transcribe/)
6. [Translate](6-Translate/)
7. [Notify](7-Notify/)
8. [Step Function](8-Step-Function/)
9. [SNS](9-SNS/)
10. [Call Step Function](10-Call-Step-Function/)
11. [Test website](11-Test-website/)
12. [Clean up resources](12-Clean-Up-Resources/)
