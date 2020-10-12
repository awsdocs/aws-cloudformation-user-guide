# Security best practices for AWS CloudFormation<a name="security-best-practices"></a>

AWS CloudFormation provides a number of security features to consider as you develop and implement your own security policies\. The following best practices are general guidelines and don’t represent a complete security solution\. Because these best practices might not be appropriate or sufficient for your environment, treat them as helpful considerations rather than prescriptions\. 

**Topics**
+ [Use IAM to control access](#use-iam-to-control-access)
+ [Do not embed credentials in your templates](#creds)
+ [Use AWS CloudTrail to log AWS CloudFormation calls](#cloudtrail)

## Use IAM to control access<a name="use-iam-to-control-access"></a>

IAM is an AWS service that you can use to manage users and their permissions in AWS\. You can use IAM with AWS CloudFormation to specify what AWS CloudFormation actions users can perform, such as viewing stack templates, creating stacks, or deleting stacks\. Furthermore, anyone managing AWS CloudFormation stacks will require permissions to resources within those stacks\. For example, if users want to use AWS CloudFormation to launch, update, or terminate Amazon EC2 instances, they must have permission to call the relevant Amazon EC2 actions\.

In most cases, users require full access to manage all of the resources in a template\. AWS CloudFormation makes calls to create, modify, and delete those resources on their behalf\. To separate permissions between a user and the AWS CloudFormation service, use a service role\. AWS CloudFormation uses the service role's policy to make calls instead of the user's policy\. For more information, see [AWS CloudFormation service role](using-iam-servicerole.md)\.

## Do not embed credentials in your templates<a name="creds"></a>

Rather than embedding sensitive information in your AWS CloudFormation templates, we recommend you use *dynamic references* in your stack template\.

Dynamic references provide a compact, powerful way for you to reference external values that are stored and managed in other services, such as the AWS Systems Manager Parameter Store or AWS Secrets Manager\. When you use a dynamic reference, CloudFormation retrieves the value of the specified reference when necessary during stack and change set operations, and passes the value to the appropriate resource\. However, CloudFormation never stores the actual reference value\. For more information, see [Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html)\.

[AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) helps you to securely encrypt, store, and retrieve credentials for your databases and other services\. The [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) provides secure, hierarchical storage for configuration data management\. 

For more information on defining template parameters, see [Parameters](parameters-section-structure.md)\.

## Use AWS CloudTrail to log AWS CloudFormation calls<a name="cloudtrail"></a>

AWS CloudTrail tracks anyone making AWS CloudFormation API calls in your AWS account\. API calls are logged whenever anyone uses the AWS CloudFormation API, the AWS CloudFormation console, a back\-end console, or AWS CloudFormation AWS CLI commands\. Enable logging and specify an Amazon S3 bucket to store the logs\. That way, if you ever need to, you can audit who made what AWS CloudFormation call in your account\. For more information, see [Logging AWS CloudFormation API calls with AWS CloudTrail](cfn-api-logging-cloudtrail.md)\.