# SESEmailForward
Amazon SES Email Forward to Your Inbox

[![Deploy Stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=SESEmailForward&templateURL=https://s3.amazonaws.com/public.cf.templates/forwarder.template)

## Usage Guide
You can deploy the CloudFormation stack which will provision the following AWS Services
- SNS Topic to forward, received emails from SES
- IAM Role to invoke Lambda function from SNS
- Lambda function with NodeJS code to forward the emails to a defined from and to address
- IAM Role allowing Lambda to forward emails.

Since AWS SES doesn't support CloudFormation at the moment, you need to create an email receiving rule from Amazon Web Console SES section and forward the email to the provisioned SNS topic (Need just to select the topic with UTF encoding).

### Sources ###
- https://medium.com/@ashan.fernando/forwarding-emails-to-your-inbox-using-amazon-ses-2d261d60e417
- https://aws.amazon.com/blogs/messaging-and-targeting/forward-incoming-email-to-an-external-destination/
- https://github.com/medmunds/aws-cfn-ses-domain
- https://stackoverflow.com/questions/47026560/do-aws-support-ses-in-cloudformation
