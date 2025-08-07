# Infrastructure Description

This document describes the infrastructure components used to host the application, including the backend API, frontend client, and database.

## 🔗 Architecture Overview
+-------------------+      +-------------------+      +-------------------+
|                   |      |                   |      |                   |
|      Client       + ---> +      S3 Bucket    + ---> + (Static Frontend) |
|   (Web Browser)   |      |                   |      |                   |
+-------------------+      +-------------------+      +-------------------+

         |
         v

+-------------------+      +-------------------+
|                   |      |                   |
| Elastic Beanstalk + ---> +      RDS          |
|    (API Server)   |      |  (Postgres DB)    |
+-------------------+      +-------------------+

         |
         v

+-------------------+
|                   |
|      S3 Bucket    |
|   (User Uploads)  |
|                   |
+-------------------+

         ^
         |
+-------------------+
|                   |
|    CircleCI       |
|   (CI/CD Pipeline)|
|                   |
+-------------------+

         |
         v

+-------------------+      +-------------------+
|                   |      |                   |
| Elastic Beanstalk |      |        S3         |
|  (API Deploy)     |      | (Frontend Deploy) |
+-------------------+      +-------------------+


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

