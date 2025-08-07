# Hosting a Full-Stack Application

# Udagram

This application is provided to you as an alternative starter project if you do not wish to host your own code done in the previous courses of this nanodegree. The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.



### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

### Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres. <Place holder for link to classroom article>
1. In AWS, provision a s3 bucket for hosting the uploaded files. <Place holder for tlink to classroom article>
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework



## Decumntation
- [Infrastructure Description](./docs/Application_dependencies.md)
- [Application Dependencies](./docs/Infrastructure_description.md)
- [Pipeline Description](./docs/Pipeline_description.md)

## Demo
A live demo for the Application can be found at [udagram][]

Frontend 
// screenshot
Backend 
// screenshot


## The deployment process and AWS resources used in this project:
// key screenshot
// Amazon RDS dashboard showing the details of the database instance.

### Amazon RDS
 RDS dashboard showing the details of the database instance.
Detailed view of the RDS instance security group configuration, including endpoint and connectivity settings.

### AWS Elastic Beanstalk 

AWS Elastic Beanstalk environment dashboard, showing the status of the deployed api.



### AWS S3 
bucket dashboard, displaying the contents of the bucket used for hosting the frontend.
public access settings, showing the configuration for allowing public access to the hosted frontend.
policy configuration, ensuring proper permissions for public access to the frontend files.
S3 bucket CORS configuration, allowing cross-origin requests from the frontend.

### CircleCI
//CircleCI dashboard overview, highlighting recent pipeline runs.
CircleCI build job details, showing successful build steps.

CircleCI deployment job details, confirming successful deployment to AWS.




## License

[License](LICENSE.txt)

