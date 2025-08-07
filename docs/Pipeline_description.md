# CI/CD Pipeline Description

This document explains the steps of the CI/CD pipeline implemented using CircleCI.


+-------------------+      +-------------------+      +-------------------+
|                   |      |                   |      |                   |
|    Push Code      +----->+   CircleCI        +----->+   Build & Test    |
|  (To Repository)  |      |  (CI/CD Pipeline) |      |    (Frontend &    |
|                   |      |                   |      |      Backend)     |
+-------------------+      +-------------------+      +-------------------+

                                      |
                                      v

                            +-------------------+
                            |                   |
                            |  Deploy Backend    |
                            |   to Elastic      |
                            |   Beanstalk       |
                            |                   |
                            +-------------------+

                                      |
                                      v

                            +-------------------+
                            |                   |
                            |  Deploy Frontend   |
                            |   to S3 Bucket    |
                            |                   |
                            +-------------------+


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

