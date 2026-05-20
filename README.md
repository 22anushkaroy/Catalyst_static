# Static Website Hosting using AWS S3 with GitHub Actions CI/CD

## Project Overview
This project demonstrates automated deployment of a static website using AWS S3 and GitHub Actions. The objective was to eliminate manual deployment by implementing a CI/CD pipeline that automatically updates the website whenever changes are pushed to the GitHub repository.

---

# Project Planning

The project was planned with the goal of creating a simple, scalable, and automated cloud deployment workflow for static websites. Instead of manually uploading website files after every update, an automated pipeline was designed using GitHub Actions and AWS services.

The workflow follows this architecture:

Local Development → Git → GitHub Repository → GitHub Actions → AWS IAM Authentication → AWS S3 Bucket → Live Static Website

The planning phase included:

- Using Git for version control and project history management
- Hosting the static website on AWS S3
- Automating deployment using GitHub Actions
- Securing deployment credentials using GitHub Secrets
- Configuring IAM authentication for AWS access
- Enabling static website hosting through S3 bucket configuration

---

# Technologies Used

- AWS S3
- AWS IAM
- Git
- GitHub
- GitHub Actions
- HTML
- CSS

---

# Features

- Static website hosting using AWS S3
- Automated CI/CD deployment pipeline
- Git-based version control
- Secure credential management using GitHub Secrets
- Automatic deployment on every push to the main branch

---

# CI/CD Workflow

1. Developer pushes code to GitHub
2. GitHub Actions workflow gets triggered
3. AWS credentials are authenticated using IAM
4. Website files are synchronized to the S3 bucket
5. Updated website becomes live automatically

---

# Security Implementation

- AWS credentials stored securely in GitHub Secrets
- IAM used for authentication and authorization
- Bucket policy configured for public website access
- Deployment access controlled through IAM permissions

---

# Challenges Faced

- Encountered `404 NoSuchKey` error due to incorrect file structure in S3
- Fixed deployment issue by ensuring `index.html` existed at the root level of the bucket
- Configured bucket policies and public access settings correctly for static hosting

---

# Future Improvements

- Implement CloudFront CDN for HTTPS and caching
- Use least-privilege IAM policies instead of AmazonS3FullAccess
- Add custom domain integration
- Implement OIDC authentication instead of long-lived access keys

---

# Conclusion

This project demonstrates practical implementation of cloud hosting, CI/CD automation, version control, deployment troubleshooting, and IAM-based security using AWS and GitHub Actions.
