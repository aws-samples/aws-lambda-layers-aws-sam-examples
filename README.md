# Creating AWS Lambda Layers using Node.js and AWS SAM

This example application shows how to build AWS Lambda Layers using Node.js and the AWS Serverless Application Model.

To learn more about how this sample works, see AWS Compute Blog post: https://aws.amazon.com/blogs/compute/using-lambda-layers-to-simplify-your-development-process/.

Important: this application uses various AWS services and there are costs associated with these services after the Free Tier usage - please see the [AWS Pricing page](https://aws.amazon.com/pricing/) for details. You are responsible for any AWS costs incurred. No warranty is implied in this example.

```bash
.
├── README.MD                   <-- This instructions file
├── aws-sdk-layer               <-- Source code for the Vue.js
├── sharp-layer                 <-- Source code for the serverless backend
```

## Requirements

* AWS CLI already configured with Administrator permission
* [AWS SAM CLI installed](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html) - minimum version 0.48.
* [NodeJS 12.x installed](https://nodejs.org/en/download/)

## Installation Instructions

1. [Create an AWS account](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html) if you do not already have one and login.

2. Clone the repo onto your local development machine using `git clone`.

3. Change into the repo's directory.

4. Run:

```
npm install
mkdir ./layer/nodejs –p
mv ./node_modules ./layer/nodejs
```
5.	Next, deploy the SAM template to create the layer:
```
sam deploy --guided
```

When prompted for parameters, enter:
- Stack Name: aws-sdk-layer
- AWS Region: your preferred AWS Region (e.g. us-east-1)
- Accept all other defaults.

6.	After the deployment completes, the new Lambda layer is available to use. Run this command to see the available layers:

```
aws lambda list-layers
```

## Next steps

The AWS Compute Blog post at the top of this README file contains additional information about the how to use Lambda layers.

If you have any questions, please raise an issue in the GitHub repo.

==============================================

Copyright 2020 Amazon.com, Inc. or its affiliates. All Rights Reserved.

SPDX-License-Identifier: MIT-0
