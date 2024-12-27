# Pipeline

Pipeline contains 2 major parts:

- Build
- Deploy

## Build

Build phase has few steps resulting in having built both Frontend and Backend API:

- preparing pipeline environment (f.e. installing Node, preparing env variables, etc.)
- checking out code from GitHub repository
- installing Frontend dependencies
- installing Backend API dependencies
- running linter for Frontend
- building Frontend
- builidng Backend API

## Deploy

Deploy phase is started after successful build and manual approve. It results in deploying Frontend and Backend API to target environment. Steps:

- preparing pipeline environment (f.e. installing Node, preparing env variables, etc.)
- configuring AWS tools (Elastic Beanstalk CLI, AWS CLI, AWS Access Key)
- checking out code from GitHub repository
- installing and building Frontend and Backend API
- setting environment variables for Backend API (by using variables securely defined in CircleCI)
- deploying new Backend API version to Elastic Beanstalk
- deploying Frontend to S3 by uploading files to S3 Bucket

## Diagram

![Pipeline diagram](./screenshots/pipeline.png)
