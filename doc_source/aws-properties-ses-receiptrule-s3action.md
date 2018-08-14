# Amazon Simple Email Service ReceiptRule S3Action<a name="aws-properties-ses-receiptrule-s3action"></a>

<a name="aws-properties-ses-receiptrule-s3action-description"></a>The `S3Action` property type includes an action in an Amazon SES receipt rule that saves the received message to an Amazon S3 bucket and, optionally, publishes a notification to Amazon SNS\.

To enable Amazon SES to write emails to your Amazon S3 bucket, use an AWS KMS key to encrypt your emails, or publish to an Amazon SNS topic of another account, Amazon SES must have permission to access those resources\. For information about giving permissions, see [Giving Permissions to Amazon SES for Email Receiving](url-ses-dev;receiving-email-permissions.html) in the *Amazon Simple Email Service Developer Guide*\. 

**Note**  
When you save your emails to an Amazon S3 bucket, the maximum email size \(including headers\) is 30 MB\. Emails larger than that will bounce\.

For information, see [S3 Action](url-ses-dev;receiving-email-action-s3.html) in the *Amazon Simple Email Service Developer Guide*\. 

<a name="aws-properties-ses-receiptrule-s3action-inheritance"></a> `S3Action` is a property of the [Amazon Simple Email Service ReceiptRule Action](aws-properties-ses-receiptrule-action.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-s3action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-s3action-syntax.json"></a>

```
{
  "[BucketName](#cfn-ses-receiptrule-s3action-bucketname)" : String,
  "[KmsKeyArn](#cfn-ses-receiptrule-s3action-kmskeyarn)" : String,
  "[TopicArn](#cfn-ses-receiptrule-s3action-topicarn)" : String,
  "[ObjectKeyPrefix](#cfn-ses-receiptrule-s3action-objectkeyprefix)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-s3action-syntax.yaml"></a>

```
[BucketName](#cfn-ses-receiptrule-s3action-bucketname): String
[KmsKeyArn](#cfn-ses-receiptrule-s3action-kmskeyarn): String
[TopicArn](#cfn-ses-receiptrule-s3action-topicarn): String
[ObjectKeyPrefix](#cfn-ses-receiptrule-s3action-objectkeyprefix): String
```

## Properties<a name="aws-properties-ses-receiptrule-s3action-properties"></a>

`BucketName`  <a name="cfn-ses-receiptrule-s3action-bucketname"></a>
The name of the Amazon S3 bucket that incoming email will be saved to\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KmsKeyArn`  <a name="cfn-ses-receiptrule-s3action-kmskeyarn"></a>
The customer master key that Amazon SES should use to encrypt your emails before saving them to the Amazon S3 bucket\. You can use the default master key or a custom master key you created in AWS KMS as follows:  
+ To use the default master key, provide an ARN in the form of `arn:aws:kms:REGION:ACCOUNT-ID-WITHOUT-HYPHENS:alias/aws/ses`\. For example, if your AWS account ID is `123456789012` and you want to use the default master key in the US West \(Oregon\) region, the ARN of the default master key would be `arn:aws:kms:us-west-2:123456789012:alias/aws/ses`\. If you use the default master key, you don't need to perform any extra steps to give Amazon SES permission to use the key\.
+ To use a custom master key you created in AWS KMS, provide the ARN of the master key and ensure that you add a statement to your key's policy to give Amazon SES permission to use it\. For more information about giving permissions, see [Giving Permissions to Amazon SES for Email Receiving](url-ses-dev;receiving-email-permissions.html) in the *Amazon Simple Email Service Developer Guide*\.
For more information about key policies, see [AWS Key Management Service Concepts](url-kms-dev;concepts.html) in the *AWS Key Management Service Developer Guide*\. If you do not specify a master key, Amazon SES will not encrypt your emails\.  
Your mail is encrypted by Amazon SES using the Amazon S3 encryption client before the mail is submitted to Amazon S3 for storage\. It is not encrypted using Amazon S3 server\-side encryption\. This means that you must use the Amazon S3 encryption client to decrypt the email after retrieving it from Amazon S3, as the service has no access to use your AWS KMS keys for decryption\. This encryption client is currently available with the AWS SDK for Java and AWS SDK for Ruby only\. For more information about client\-side encryption using AWS KMS master keys, see [Protecting Data Using Client\-Side Encryption](url-s3-dev;UsingClientSideEncryption.html) in the *Amazon Simple Storage Service Developer Guide*\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ObjectKeyPrefix`  <a name="cfn-ses-receiptrule-s3action-objectkeyprefix"></a>
The key prefix of the Amazon S3 bucket\. The key prefix is similar to a directory name that enables you to store similar data under the same directory in a bucket\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TopicArn`  <a name="cfn-ses-receiptrule-s3action-topicarn"></a>
The ARN of the Amazon SNS topic to notify when the message is saved to the Amazon S3 bucket\. An example of an Amazon SNS topic ARN is `arn:aws:sns:us-west-2:123456789012:MyTopic`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-s3action-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [Giving Permissions to Amazon SES for Email Receiving](url-ses-dev;receiving-email-permissions.html) in the *Amazon Simple Email Service Developer Guide*
+ [S3 Action](url-ses-dev;receiving-email-action-s3.html) in the *Amazon Simple Email Service Developer Guide*
+ [S3Action](url-ses-api;API_S3Action.html) in the *Amazon Simple Email Service API Reference*