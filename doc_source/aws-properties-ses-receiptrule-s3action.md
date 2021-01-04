# AWS::SES::ReceiptRule S3Action<a name="aws-properties-ses-receiptrule-s3action"></a>

When included in a receipt rule, this action saves the received message to an Amazon Simple Storage Service \(Amazon S3\) bucket and, optionally, publishes a notification to Amazon Simple Notification Service \(Amazon SNS\)\.

To enable Amazon SES to write emails to your Amazon S3 bucket, use an AWS KMS key to encrypt your emails, or publish to an Amazon SNS topic of another account, Amazon SES must have permission to access those resources\. For information about giving permissions, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-permissions.html)\.

**Note**  
When you save your emails to an Amazon S3 bucket, the maximum email size \(including headers\) is 30 MB\. Emails that are larger than 30 MB aren't saved\.

For information about specifying Amazon S3 actions in receipt rules, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-action-s3.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-s3action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-s3action-syntax.json"></a>

```
{
  "[BucketName](#cfn-ses-receiptrule-s3action-bucketname)" : String,
  "[KmsKeyArn](#cfn-ses-receiptrule-s3action-kmskeyarn)" : String,
  "[ObjectKeyPrefix](#cfn-ses-receiptrule-s3action-objectkeyprefix)" : String,
  "[TopicArn](#cfn-ses-receiptrule-s3action-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-s3action-syntax.yaml"></a>

```
  [BucketName](#cfn-ses-receiptrule-s3action-bucketname): String
  [KmsKeyArn](#cfn-ses-receiptrule-s3action-kmskeyarn): String
  [ObjectKeyPrefix](#cfn-ses-receiptrule-s3action-objectkeyprefix): String
  [TopicArn](#cfn-ses-receiptrule-s3action-topicarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-s3action-properties"></a>

`BucketName`  <a name="cfn-ses-receiptrule-s3action-bucketname"></a>
The name of the Amazon S3 bucket that you want to send incoming mail to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-ses-receiptrule-s3action-kmskeyarn"></a>
The customer master key that Amazon SES should use to encrypt your emails before saving them to the Amazon S3 bucket\. You can use the default master key or a custom master key that you created in AWS KMS as follows:  
+ To use the default master key, provide an ARN in the form of `arn:aws:kms:REGION:ACCOUNT-ID-WITHOUT-HYPHENS:alias/aws/ses`\. For example, if your AWS account ID is 123456789012 and you want to use the default master key in the US West \(Oregon\) Region, the ARN of the default master key would be `arn:aws:kms:us-west-2:123456789012:alias/aws/ses`\. If you use the default master key, you don't need to perform any extra steps to give Amazon SES permission to use the key\.
+ To use a custom master key that you created in AWS KMS, provide the ARN of the master key and ensure that you add a statement to your key's policy to give Amazon SES permission to use it\. For more information about giving permissions, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-permissions.html)\.
For more information about key policies, see the [AWS KMS Developer Guide](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html)\. If you don't specify a master key, Amazon SES doesn't encrypt your emails\.  
Your mail is encrypted by Amazon SES using the Amazon S3 encryption client before the mail is submitted to Amazon S3 for storage\. It isn't encrypted using Amazon S3 server\-side encryption\. This means that you must use the Amazon S3 encryption client to decrypt the email after retrieving it from Amazon S3, as the service has no access to use your AWS KMS keys for decryption\. This encryption client is currently available with the [AWS SDK for Java](http://aws.amazon.com/sdk-for-java/) and [AWS SDK for Ruby](http://aws.amazon.com/sdk-for-ruby/) only\. For more information about client\-side encryption using AWS KMS master keys, see the [Amazon S3 Developer Guide](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingClientSideEncryption.html)\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectKeyPrefix`  <a name="cfn-ses-receiptrule-s3action-objectkeyprefix"></a>
The key prefix of the Amazon S3 bucket\. The key prefix is similar to a directory name that enables you to store similar data under the same directory in a bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicArn`  <a name="cfn-ses-receiptrule-s3action-topicarn"></a>
The ARN of the Amazon SNS topic to notify when the message is saved to the Amazon S3 bucket\. You can find the ARN of a topic by using the [ListTopics](https://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html) operation in the Amazon SNS API\.  
For more information about Amazon SNS topics, see the [Amazon SNS Developer Guide](https://docs.aws.amazon.com/sns/latest/dg/CreateTopic.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ses-receiptrule-s3action--examples"></a>

### S3 Action in SES RuleSet<a name="aws-properties-ses-receiptrule-s3action--examples--S3_Action_in_SES_RuleSet"></a>

The following example creates an S3 Action in a SES RuleSet\. 

#### JSON<a name="aws-properties-ses-receiptrule-s3action--examples--S3_Action_in_SES_RuleSet--json"></a>

```
{
    "SesRuleSet": {
        "Type": "AWS::SES::ReceiptRuleSet"
    },
    "SesRule": {
        "Type": "AWS::SES::ReceiptRule",
        "Properties": {
            "Rule": {
                "Recipients": [
                    "String"
                ],
                "Actions": [
                    {
                        "S3Action": {
                            "BucketName": {
                                "Ref": "Bucket"
                            }
                        }
                    }
                ],
                "Enabled": true,
                "ScanEnabled": true
            },
            "RuleSetName": {
                "Ref": "SesRuleSet"
            }
        }
    }
}
```

#### YAML<a name="aws-properties-ses-receiptrule-s3action--examples--S3_Action_in_SES_RuleSet--yaml"></a>

```
SesRuleSet:
  Type: 'AWS::SES::ReceiptRuleSet'
SesRule:
  Type: 'AWS::SES::ReceiptRule'
  Properties:
    Rule:
      Recipients:
        - String
      Actions:
        - S3Action:
            BucketName: !Ref Bucket
      Enabled: true
      ScanEnabled: true
    RuleSetName: !Ref SesRuleSet
```