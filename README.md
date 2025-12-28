# Amazon S3 Static Website Hosting

This project demonstrates how to host a static website using an Amazon S3 bucket.  
Amazon S3 provides a simple, scalable, and cost-effective way to host static websites
without managing servers.


## Prerequisites

- An AWS account
- Basic knowledge of AWS Console
- Static website files (HTML, CSS, JavaScript)
- Internet access


## Step 1: Create an S3 Bucket

1. Sign in to the **AWS Management Console**
2. Navigate to **S3**
3. Click **Create bucket**
4. Enter a **globally unique bucket name**
<br>
<p align="center">
  <img src="images/1.png" width="500">
  
  <img src="images/2.png" width="500">
</p>
<br>

6. Uncheck **Block all public access**
7. Acknowledge the warning and create the bucket
<br>
<p align="center" >
  <img src="images/3.png" width="500">
  <img src="images/4.png" width="500">
</p>
<br>

## Step 2: Upload Website Files

1. Open the created bucket
<br>
<p align="center">
  <img src="images/5.png" width="500">
</p>
<br>

3. Click **Upload**
<br>
<p align="center">
  <img src="images/6.png" width="500">
</p>
<br>

4. Upload your static files:
   - `index.html`
   - `error.html`
   - CSS, JS, images, etc. (optional)

  <br>
<p align="center">
  <img src="images/7.png" width="500">
  <img src="images/8.png" width="500">
</p>
<br>

5. Click **Upload**

<br>
<p align="center">
  <img src="images/9.png" width="500">
</p>
<br>

## Step 3: Enable Static Website Hosting

1. Go to the **Properties** tab of the bucket

<br>
<p align="center">
  <img src="images/12.png" width="500">
</p>
<br>

2. Scroll to **Static website hosting**
3. Click **Edit**

<br>
<p align="center">
  <img src="images/13.png" width="500">
</p>
<br>

4. Select **Enable**
5. Enter:
   - **Index document:** `index.html`
   - **Error document:** `error.html` (optional)

<br>
<p align="center">
  <img src="images/14.png" width="500">
</p>
<br>

6. Save changes

<br>
<p align="center">
  <img src="images/15.png" width="500">
</p>
<br>

## Step 4: Configure Bucket Policy for Public Access

1. Go to the **Permissions** tab

<br>
<p align="center">
  <img src="images/10.png" width="500">
</p>
<br>

2. Open **Bucket policy**
3. Add the following policy (replace `YOUR_BUCKET_NAME`):

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
```
<br>
<p align="center">
  <img src="images/11.png" width="500">
</p>
<br>

4. Save the policy

## Step 5: Navigate to the Public Website Link

1. Go to the **Properties** tab of the S3 bucket
2. Scroll down to **Static website hosting**
3. Locate the **Bucket website endpoint**
4. Click the endpoint link or copy it into your browser

<br>
<p align="center">
  <img src="images/15.png" width="500">
</p>
<br>

**Your Amazon S3 static website is now officially deployed and live!** 🚀
<br>

<p align="center">
  <img src="images/16.png" width="500">
</p>
<br>

## Credits 
We gratefully acknowledge the contributions of: 
- Kushal (https://github.com/Kushal-dev-22)
- Harmila (https://github.com/Harmila331)
- Dhanaswi (https://github.com/dhanaswi)

