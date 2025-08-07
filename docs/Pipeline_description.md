# CI/CD Pipeline Description

This document explains the steps of the CI/CD pipeline implemented using CircleCI.

<img width="987" height="830" alt="image" src="https://github.com/user-attachments/assets/b943524b-a2c9-40fb-8a02-4338878723f2" />



## Steps Overview

1. **Checkout Code**
   - Pulls latest code from GitHub repo

2. **Install Dependencies**
   - Installs frontend and backend dependencies using npm

3. **Run Tests**
   - Executes automated tests for the backend API

4. **Build Frontend**
   - Compiles and optimizes frontend assets

5. **Deploy Backend to Elastic Beanstalk**
   - Deploys the built backend to an EB environment using the EB CLI

6. **Deploy Frontend to S3**
   - Uploads the built frontend assets to an S3 bucket

