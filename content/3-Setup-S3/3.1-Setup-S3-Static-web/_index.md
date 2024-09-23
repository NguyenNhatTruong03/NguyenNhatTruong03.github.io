---
title : "Setup S3 Static website"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

## Create S3 Bucket

Go to the S3 dashboard and create a new Bucket named **`web-translate-ws-2024`**

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n1.png)

Select **ACLs enable** and check **Object write to make objects in the bucket public.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n2.png)

Uncheck **Block all public access*, check **

I acknowledge that the current settings might result in this bucket and the objects within becoming public.** to allow other sources to access S3

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n.png)

**Create bucket**

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n3.png)

Select the newly created Bucket and go to **Premissions**.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n4.png)

Go to **Bucket policy** to configure the Bucket policy.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n5.png)

Configure the policy for the bucket using the **Policy generator** feature.

{{% notice note %}}
Before selecting **Policy generator**, you need to copy **Bucket ARN**
{{% /notice %}}

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n6.png)

Configure to create a policy for the bucket.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n7.png)

Check that you have selected all the actions that can be performed with this bucket, the correct bucket arn.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n8.png)

After selecting **Generate Policy**, you will get the json policy code and copy this code.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n9.png)

Paste the code.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n10.png)

{{% notice note %}}
At the end of the **Resource** line, add /* to allow access to objects in the bucket.
{{% /notice %}}

**Save changes**

Upload the website code file to the bucket, select upload and select the file to upload and finally click **Upload**.

Download 2 code files:

- [index.html](https://drive.google.com/file/d/19ekeJsFYAZ-6qJIxMpHMbSsAyPruH26K/view?usp=sharing)

- [video-player.html](https://drive.google.com/file/d/1_S934h-snq5G-GxGSgEQrSX-eMHarYYn/view?usp=drive_link)

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n11.png)

Create static website hosting in **Properties** then go to **Static website hosting**.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n15.png)

Configure static website hosting.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n13.png)

{{% notice note %}}
In the **Index document** section, enter the file name you want to display first, or maybe as the homepage. Leave the same name as the file uploaded to the Bucket. **Error document** if you code a file to display website errors, you can upload it and leave the name of that file, here because there is no file to display errors in the interface, you can leave the file name as **Index document**.
{{% /notice %}}

**Save changes**

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n14.png)

That's it and there will be a link to the website.

![Sep-Up-S3](/images/3.setupS3/3.1.ima/n16.png)