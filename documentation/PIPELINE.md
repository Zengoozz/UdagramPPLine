# Pipeline Process

## Understanding pipeline with CircleCi

1. Need to configure `.circleci/config.yml` to put your work flow in.
1. Orbs are open-source, shareable packages of parameterizable reusable configuration elements, including jobs, commands, and executors. Use orbs to reduce configuration complexity and help you integrate with your software and services stack quickly and easily across many projects such as node and aws-cli.
1. Steps are the sequence the application will be run through to perform specific job.

## Integrate CircleCi

1. Login with github account which contain the project want to integrate it with circleci.
1. Setup the project and ensure it has `.circleci/config.yml`
1. commit your project changes and push it to your repository to run the jobs written in config file.

## Udagram CircleCi Process Sequence

- Installing node.js, AWS CLI.
- Setting up EB CLI.
- Checkout code.
- Installing, building and deploying frontend.
- Installing, building and deploying backend.