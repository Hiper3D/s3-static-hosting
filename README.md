# ☁️ AWS Cloud Infrastructure: Secure Portfolio Deployment

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon%20S3-569A31?style=for-the-badge&logo=Amazon%20S3&logoColor=white)
![Amazon CloudFront](https://img.shields.io/badge/Amazon%20CloudFront-8C4FFF?style=for-the-badge&logo=Amazon%20CloudFront&logoColor=white)
![Security](https://img.shields.io/badge/Security-OAC%20Enforced-brightgreen?style=for-the-badge)

## 📋 Project Overview
This repository serves as the Infrastructure Documentation for my personal portfolio website. To demonstrate practical cloud engineering skills, I decoupled the application code from its hosting environment. I successfully migrated the deployment from a fully managed PaaS [Platform as a Service - a cloud computing model that provides a platform allowing customers to develop, run, and manage applications] to a custom, production-grade AWS [Amazon Web Services - a comprehensive cloud computing platform] infrastructure.

💻 **Application Source Code:** [View the MyPortfolio Repository Here](https://github.com/Hiper3D/MyPortfolio)

## 🚀 Live Environment
**Production URL:** [https://d1m1fa948besma.cloudfront.net](https://d1m1fa948besma.cloudfront.net)

*(Note: The application is now globally distributed and strictly enforces HTTPS [Hypertext Transfer Protocol Secure - the encrypted and secure version of the standard web protocol] traffic for end-to-end encryption).*

---

## 📈 Architectural Evolution & Migration History
This project represents a multi-month cloud migration, transitioning from a managed PaaS to a custom, highly secure AWS infrastructure.

### Phase 1: Managed Hosting (Vercel)
* **Initial Setup:** Source code was maintained in a dedicated GitHub repository and linked to Vercel for automated, managed hosting.
* **Limitation:** While fast to deploy, this PaaS model abstracted away the underlying infrastructure, offering no hands-on control over networking, storage, or security policies.

### Phase 2: AWS Migration (Amazon S3)
* **Action:** Decoupled the application from Vercel to build custom cloud infrastructure. 
* **Implementation:** Uploaded static assets directly to an Amazon S3 [Simple Storage Service - an object storage service provided by Amazon for storing files] bucket in the `ap-south-1` region configured for public website hosting. Created this dedicated infrastructure repository to document the architecture.
* **Limitation:** The site was functional but served over unencrypted HTTP [Hypertext Transfer Protocol - the foundation of data communication for the World Wide Web], lacking enterprise-grade security and global caching.

### Phase 3: Production-Grade Security (Current)
* **Action:** Upgraded the S3 deployment into a secure, globally distributed architecture.
* **Implementation:** Provisioned an Amazon CloudFront [Content Delivery Network - a geographically distributed network of servers to deliver content faster] distribution. Secured the origin bucket by disabling public access and enforcing OAC [Origin Access Control - a security feature that restricts access to your storage so only your distribution can read it].
* **Outcome:** The portfolio is now globally cached at Edge Locations and strictly enforces HTTPS traffic, achieving a zero-trust storage model.

---

## 🗺️ Roadmap & Next Steps
* **Custom DNS Routing:** Map a custom professional domain to the CloudFront distribution using Amazon Route 53 and provision a custom certificate.
* **CI/CD Pipeline:** Implement GitHub Actions to automate the synchronization of local repository changes directly to the S3 bucket.
