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

##

- Open IDE and run below

```
npm install -g npm@9.7.2
serverless create --template aws-nodejs
serverless deploy
```
# basic-lambda
