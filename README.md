# AWS S3 Static Website Hosting

## Project Overview
This project demonstrates how to host a static website using Amazon S3.  
The website files such as HTML, CSS, JavaScript, and images are stored in an S3 bucket and served publicly using AWS Static Website Hosting.

---

## Technologies Used
- Amazon S3
- AWS IAM
- HTML5
- CSS3
- Git & GitHub

---

## Project Features
- Static website hosting using Amazon S3
- Public website accessibility
- Custom index and error pages
- Easy deployment and low-cost hosting
- Beginner-friendly AWS cloud project

---

## Project Architecture

User Browser → AWS S3 Bucket → Static Website

---

## Project Files

AWS-S3-Static-Website/
│
├── index.html
├── error.html
├── style.css
├── README.md
└── screenshots/

---

## Steps Performed

### 1. Created an S3 Bucket
- Opened AWS S3 Console
- Created a unique bucket
- Selected AWS region

### 2. Uploaded Website Files
- Uploaded HTML, CSS, JS, and image files

### 3. Disabled Block Public Access
- Allowed public access to website files

### 4. Added Bucket Policy
Used bucket policy to allow public read access.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}
