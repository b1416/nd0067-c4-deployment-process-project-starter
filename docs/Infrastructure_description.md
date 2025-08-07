# Infrastructure Description

This document describes the infrastructure components used to host the application, including the backend API, frontend client, and database.

## 🔗 Architecture Overview
<img width="536" height="331" alt="image" src="https://github.com/user-attachments/assets/8b8e8639-6f0c-4f24-abc2-b2a37472f025" />


## Components
### 1. **Elastic Beanstalk (EB)**
- Used to host the **Node.js backend API**
- Automatically handles load balancing and environment provisioning

### 2. **RDS (PostgreSQL)**
- PostgreSQL database hosted in a private subnet
- Used by the backend for data persistence

### 3. **Amazon S3**
- Hosts the static **frontend (React or Angular)**
- Configured for public read access with proper CORS and policy settings

### 4. **IAM Roles**
- Provide limited access to EB and S3 via CI/CD pipeline
- Secrets and credentials are passed as environment variables

