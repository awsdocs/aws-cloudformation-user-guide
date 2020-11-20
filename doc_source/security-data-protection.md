# Data protection in AWS CloudFormation<a name="security-data-protection"></a>

The AWS [shared responsibility model](http://aws.amazon.com/compliance/shared-responsibility-model/) applies to data protection in AWS CloudFormation\. As described in this model, AWS is responsible for protecting the global infrastructure that runs all of the AWS Cloud\. You are responsible for maintaining control over your content that is hosted on this infrastructure\. This content includes the security configuration and management tasks for the AWS services that you use\. For more information about data privacy, see the [Data Privacy FAQ](http://aws.amazon.com/compliance/data-privacy-faq)\. For information about data protection in Europe, see the [AWS Shared Responsibility Model and GDPR](http://aws.amazon.com/blogs/security/the-aws-shared-responsibility-model-and-gdpr/) blog post on the *AWS Security Blog*\.

For data protection purposes, we recommend that you protect AWS account credentials and set up individual user accounts with AWS Identity and Access Management \(IAM\)\. That way each user is given only the permissions necessary to fulfill their job duties\. We also recommend that you secure your data in the following ways:
+ Use multi\-factor authentication \(MFA\) with each account\.
+ Use SSL/TLS to communicate with AWS resources\. We recommend TLS 1\.2 or later\.
+ Set up API and user activity logging with AWS CloudTrail\.
+ Use AWS encryption solutions, along with all default security controls within AWS services\.
+ Use advanced managed security services such as Amazon Macie, which assists in discovering and securing personal data that is stored in Amazon S3\.
+ If you require FIPS 140\-2 validated cryptographic modules when accessing AWS through a command line interface or an API, use a FIPS endpoint\. For more information about the available FIPS endpoints, see [Federal Information Processing Standard \(FIPS\) 140\-2](http://aws.amazon.com/compliance/fips/)\.

We strongly recommend that you never put sensitive identifying information, such as your customers' account numbers, into free\-form fields such as a **Name** field\. This includes when you work with AWS CloudFormation or other AWS services using the console, API, AWS CLI, or AWS SDKs\. Any data that you enter into AWS CloudFormation or other services might get picked up for inclusion in diagnostic logs\. When you provide a URL to an external server, don't include credentials information in the URL to validate your request to that server\.

## Encryption at rest<a name="security-data-protection-encryption-at-rest"></a>

Following the AWS shared responsibility model, AWS CloudFormation stores your data encrypted at rest\. Customers are responsible for setting encryption and storage policies for data stored in their accounts\. For example, we recommend enabling at\-rest encryption for templates and other data stored in S3 buckets or SNS topics\. Customers similarly define encryption settings for any data storage systems provisioned by CloudFormation\.

## Encryption in transit<a name="security-data-protection-encryption-in-trainsit"></a>

AWS CloudFormation uses encrypted channels for service communications under the shared responsibility model\.

## Internetwork traffic privacy<a name="security-data-protection-internetwork-traffic-privacy"></a>

AWS CloudFormation service communications are securely encrypted by default between Regions or Availability Zones\.