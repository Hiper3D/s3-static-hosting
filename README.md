# s3-static-hosting
AWS Cloud Infrastructure: Static Website Hosting
Project Overview
This repository contains the source code for my personal portfolio, which I recently migrated from Vercel (a fully managed deployment platform) to custom AWS infrastructure. The goal of this migration was to gain hands-on experience provisioning cloud storage, managing IAM (Identity and Access Management - a web service that helps you securely control access to AWS resources) policies, and architecting secure cloud deployments.

Live Demo
Current Endpoint: http://first-demo-757038.s3-website.ap-south-1.amazonaws.com
(Note: Currently awaiting AWS account verification to implement CloudFront and custom DNS routing)

Cloud Architecture & Security
Storage: Provisioned an Amazon S3 (Simple Storage Service - an object storage service offering high scalability and security) bucket in the ap-south-1 region to host static assets and optimize regional latency.

Security Best Practices: Intentionally disabled legacy ACLs (Access Control Lists - older, less secure rules that specify which users can access individual files).

Access Control: Implemented "Bucket Owner Enforced" settings and authored custom JSON (JavaScript Object Notation - a lightweight data-interchange format) bucket policies to centrally and securely manage s3:GetObject public read access.

Next Steps (Planned Architecture)
Provision an AWS CloudFront CDN (Content Delivery Network - a geographically distributed network of servers to deliver content faster) to globally cache the site.

Secure the application with a free SSL (Secure Sockets Layer - the standard technology for keeping an internet connection secure) certificate via AWS ACM (AWS Certificate Manager - a service that lets you easily provision, manage, and deploy public and private SSL/TLS certificates).
