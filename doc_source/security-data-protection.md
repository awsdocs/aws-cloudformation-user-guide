# Data protection in AWS CloudFormation<a name="security-data-protection"></a>

AWS CloudFormation conforms to the AWS [shared responsibility model](http://aws.amazon.com/compliance/shared-responsibility-model/), which includes regulations and guidelines for data protection\. AWS is responsible for protecting the global infrastructure that runs all the AWS services\. AWS maintains control over data hosted on this infrastructure, including the security configuration controls for handling customer content and personal data\. AWS customers and APN partners, acting either as data controllers or data processors, are responsible for any personal data that they put in the AWS Cloud\. 

For data protection purposes, we recommend that you protect AWS account credentials and set up individual user accounts with AWS Identity and Access Management \(IAM\), so that each user is given only the permissions necessary to fulfill their job duties\. We also recommend that you secure your data in the following ways:
+ Use multi\-factor authentication \(MFA\) with each account\.
+ Use SSL/TLS to communicate with AWS resources\.
+ Set up API and user activity logging with AWS CloudTrail\.
+ Use AWS encryption solutions, along with all default security controls within AWS services\.
+ Use advanced managed security services such as Amazon Macie, which assists in discovering and securing personal data that is stored in Amazon S3\.

We strongly recommend that you never put sensitive identifying information, such as your customers' account numbers, into free\-form fields such as a **Name** field\. This includes when you work with AWS CloudFormation or other AWS services using the console, API, AWS CLI, or AWS SDKs\. Any data that you enter into AWS CloudFormation or other services might get picked up for inclusion in diagnostic logs\. When you provide a URL to an external server, don't include credentials information in the URL to validate your request to that server\.

For more information about data protection, see the [AWS Shared Responsibility Model and GDPR](http://aws.amazon.com/blogs/security/the-aws-shared-responsibility-model-and-gdpr/) blog post on the *AWS Security Blog*\.

## Encryption at rest<a name="security-data-protection-encryption-at-rest"></a>

Following the AWS shared responsibility model, AWS CloudFormation stores your data encrypted at rest\. Customers are responsible for setting encryption and storage policies for data stored in their accounts\. For example, we recommend enabling at\-rest encryption for templates and other data stored in S3 buckets or SNS topics\. Customers similarly define encryption settings for any data storage systems provisioned by CloudFormation\.

## Encryption in transit<a name="security-data-protection-encryption-in-trainsit"></a>

AWS CloudFormation uses encrypted channels for service communications under the shared responsibility model\.

## Internetwork traffic privacy<a name="security-data-protection-internetwork-traffic-privacy"></a>

AWS CloudFormation service communications are securely encrypted by default between Regions or Availability Zones\.