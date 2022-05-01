# Udagram Full-Stack Web Application

- Application deployed version is available at [S3 Bucket](http://pipelineprojectbucket.s3-website-us-east-1.amazonaws.com).
- Infrastructure illustration diagram is provided in  `media/InfrastructureDiagram`.
- CircleCi environment variables screenshot is provided in `media/CircleCiEnv`.
- RDS connectivity test via PgAdmin screenshot is provided in `media/PgAdmin`.
- User creation to document RDS connection success screenshot is provided in `media/createUser`.
- Elastic beanstalk environment health screenshot is provided in `media/ebHealth`.
- S3 bucket for deployed frontend screenshot is provided in `media/bucket`.

## Getting Started

1. Clone this repo locally into the location of your choice.
1. Open a terminal and navigate to the root of the repo.
1. To install from scratch follow the instructions in the installation step.


### Dependencies

```
- Node v16.13.2 or more recent.

- npm v8.1.2 or more recent.

- AWS CLI v2, v1 can work but was not tested for this project.

- A RDS database running Postgres.

- An Elastic BeanStalk environment for hosting the api.

- Two S3 buckets for hosting Front-End & uploaded pictures.

```

### Installation from Scratch

Provision the necessary AWS services needed for running the application:

1. In AWS, create a publicly available RDS database running Postgres.
1. In AWS, create a s3 bucket for hosting the uploaded files.
1. In AWS, create a elastic beanstalk environment for hosting the api.
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. Import elastic beanstalk environment link in apiHost variable in the environment files inside `frontend/src/environments`.
1. From backend folder `cd backend` Configure AWS and Elastic Beanstalk using `aws configure` then edit .elasticbeanstalk/config.yml [environment, application_name, default_region] with the current values.
1. From the root of the repo run `npm run backend:install`. After installation is done start running `npm run backend:build` and then deploy to elastic beanstalk environment by running `npm run backend:deploy`.
1. From the root of the repo run `npm run frontend:install`. After installation is done start running `npm run frontend:build` and then edit `frontend/bin/deploy.sh` to be `aws s3 cp --recursive --acl public-read ./www s3://$Bucket_name/`. After editing deploy.sh file start deploying to aws bucket by running `npm run backend:deploy` .

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd frontend`
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

