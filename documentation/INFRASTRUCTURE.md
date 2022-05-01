# Infrastructure Description

## S3 Bucket

- Can be used as a storage to host the deployed frontend on it.
- Can be used as a storage to store the media imported to the application.

## RDS

- Can be used to create a database of any type `Postgres` to connect it with the application through the EB environment.

## Elastic BeanStalk 

- Can be used to create environment to deploy the api on it in order to import it to the deployed frontend on S3 bucket and communicate with the database on RDS.
- Can be used to export environment variables from CircleCi.

## AWS CLI

- Used to authenticate the connection to the AWS to deploy frontend and backend.