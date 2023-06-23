# Create Lambda in AWS

## Create User in AWS

In Identity and Access Manaagement in AWS (IAM), add user and user group with below details for execute and deploy lambda function to AWS

1. Create User name: lambda-user
2. Create User Group: lambda-group

- AWSLambdaRole - Default policy for AWS Lambda service role.
- IAMFullAccess - Provides full access to IAM via the AWS Management Console.
- CloudWatchLogsFullAccess - Provides full access to CloudWatch Logs
- AWSCloudFormationFullAccess - Provides full access to AWS CloudFormation.
- AWSLambda_FullAccess - Grants full access to AWS Lambda service, AWS Lambda console features, and ...

## Create Access Key for the user

1. In Users, select lambda-user,
2. Go to "Security credentials" tab, click "Create Access keys"
3. In Use case: Other, click Next
4. In Description: lambda-key
5. Copy the ACCESS_KEY and SECRET_ACCESS_KEY
6. In github settings, create the repository secret
   - AWS_ACCESS_KEY_ID=<ACCESS_KEY>
   - AWS_SECRET_ACCESS_KEY=<SECRET_ACCESS_KEY>

## Develop the lambda functions

1. Open IDE and run below

- Install serverless framework

```
npm install -g serverless
```

- Create boilerplate lambda code

```
serverless create --template aws-nodejs
```

- Create main.yaml by copying the yaml content in https://github.com/serverless/github-action

- Deploy by commiting the main.yaml, it will auto deploy by github action

- Check the lambda function is deployed
  Goto Lambda in AWS

## Problem solving:

- Error: Stack:arn:aws:cloudformation is in ROLLBACK_COMPLETE state and can not be updated.
  This happens when the previous build is not successful, to resolve, please go to Cloudformation in AWS and manually delete the stack.

# basic-lambda
