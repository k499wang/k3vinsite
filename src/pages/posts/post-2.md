---
layout: ../../layouts/Blog.astro
title: "My Cloud Resume"
date: "2024-10-13"
description: "Following the Cloud Resume Challenge"
author: "Kevin"
---

You can find my resume here: https://k3-vin-wvng-resume.works/

# Introduction
As an enthusiastic newcomer to the Computer Science field, I’m eager to explore and deepen my knowledge of emerging technologies. To kickstart my journey, I took on this challenge to learn about the AWS ecosystem and its powerful services. This experience has been transformative, helping me build foundational skills in AWS and cloud computing. Below, I outline the most valuable lessons learned during this project.

Here are my repositories btw: 
[GitHub Repository: k3vin-s-resume](https://github.com/k499wang/k3vin-s-resume)
[Infrastructure as Code Repository: resume-iac-code](https://github.com/k499wang/resume-iac-code)

## Accomplishments 

1. Setting Up an S3 Bucket for Static Hosting
Creating an S3 bucket to host static content is straightforward and serves as the foundation of the project. I configured my bucket with the following key settings:

*Static Website Hosting*: I enabled static website hosting and set resume.html as the index document, which allows visitors to access my resume directly.
*Block Public Access*: Initially, I unblocked public access to configure my website but later ensured to set this to block all public access. This step is crucial for protecting sensitive data from unauthorized exposure.

2. Leveraging CloudFront as a CDN
Using CloudFront as a Content Delivery Network (CDN) proved to be a game-changer. It acts as a secure layer between users and my S3 bucket. The benefits include:

Improved Load Times: CloudFront caches content at edge locations globally, significantly speeding up access for users.
Enhanced Security: By serving content through CloudFront, I could restrict direct access to my S3 bucket, reducing the risk of potential data breaches.
HTTPS Support: CloudFront provides secure HTTPS endpoints, ensuring that all data transferred between users and the website is encrypted.

3. Understanding IAM Policies and Access Control
Setting up appropriate IAM policies was essential for managing access to both my S3 bucket and DynamoDB. For example, I created a policy that allowed my Lambda function to interact with a specific DynamoDB table while blocking access to others. This granular control is crucial for minimizing security risks and ensuring that only authorized services can access sensitive data.

4. Requesting SSL Certificates
To serve my website securely, I requested an SSL certificate through AWS Certificate Manager (ACM). This step was necessary for enabling HTTPS support on my CloudFront distribution, providing an extra layer of security for my users.

5. Configuring Custom DNS Records
Pointing my domain to the CloudFront distribution involved setting up custom DNS records. This task was relatively simple but critical, as it ensured that visitors could access my resume through a professional domain name rather than a long URL.

6. Setting Up a Lambda Function
The Lambda function serves various purposes, such as processing data or interacting with other AWS services. In my case, I allowed public access to the function URL but implemented CORS (Cross-Origin Resource Sharing) to ensure that only my website domain could make requests to it. This configuration prevents unauthorized websites from accessing my Lambda function, maintaining the security of my backend processes.

7. Handling Caching and Object Invalidation in CloudFront
I encountered challenges with CloudFront caching not updating on file changes in S3. After modifying objects, I needed to invalidate the CloudFront cache manually to ensure users received the latest content. This step highlighted the importance of understanding CDN behavior and how it impacts content delivery.

8. Troubleshooting DynamoDB Integration
During Lambda function development, I faced access issues with DynamoDB due to permission misconfigurations. Creating a refined IAM policy resolved these errors, highlighting the need for precise permissions and troubleshooting skills when working with cloud databases.

This AWS project has been invaluable in expanding my understanding of cloud technologies. Beyond technical skills, it underscored the importance of security, efficient data handling, and scalable infrastructure in modern web development. These foundational experiences have motivated me to continue exploring cloud solutions and leveraging them to build more resilient and secure applications. As I advance in my career, I’m excited to apply these skills to new challenges and further expand my expertise in cloud computing.