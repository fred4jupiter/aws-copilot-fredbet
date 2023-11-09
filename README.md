# aws-copilot-fredbet

Sample deployment of the [fredbet](https://github.com/fred4jupiter/fredbet) application using 
the [AWS Copilot CLI](https://aws.github.io/copilot-cli/).

## Running fredbet in AWS ECS

Be sure you have the AWS Copilot CLI installed. See [installation instructions](https://aws.github.io/copilot-cli/docs/getting-started/install/)
for more details.

>**Run the commands from the git root directory!**

### Create the environment

Deploys and synchronizes the changes in manifest files with CloudFormation stack:

    copilot env init
    copilot env deploy --name test

### Deploy the application/service

    copilot svc deploy --name fredbet-service --env test

## Cleanup resources

### Delete the app

    copilot app delete

Deletes all resources associated with an application.

### Delete the service

    copilot svc delete

### Delete the test environment

    copilot env delete --name test