# AWS::S3::Bucket TopicConfiguration<a name="aws-properties-s3-bucket-topicconfiguration"></a>

A container for specifying the configuration for publication of messages to an Amazon Simple Notification Service \(Amazon SNS\) topic when Amazon S3 detects specified events\.

## Syntax<a name="aws-properties-s3-bucket-topicconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-topicconfiguration-syntax.json"></a>

```
{
  "[Event](#cfn-s3-bucket-topicconfiguration-event)" : String,
  "[Filter](#cfn-s3-bucket-topicconfiguration-filter)" : NotificationFilter,
  "[Topic](#cfn-s3-bucket-topicconfiguration-topic)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-topicconfiguration-syntax.yaml"></a>

```
  [Event](#cfn-s3-bucket-topicconfiguration-event): String
  [Filter](#cfn-s3-bucket-topicconfiguration-filter): 
    NotificationFilter
  [Topic](#cfn-s3-bucket-topicconfiguration-topic): String
```

## Properties<a name="aws-properties-s3-bucket-topicconfiguration-properties"></a>

`Event`  <a name="cfn-s3-bucket-topicconfiguration-event"></a>
The Amazon S3 bucket event about which to send notifications\. For more information, see [Supported Event Types](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon S3 User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-s3-bucket-topicconfiguration-filter"></a>
The filtering rules that determine for which objects to send notifications\. For example, you can create a filter so that Amazon S3 sends notifications only when image files with a `.jpg` extension are added to the bucket\.  
*Required*: No  
*Type*: [NotificationFilter](aws-properties-s3-bucket-notificationfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Topic`  <a name="cfn-s3-bucket-topicconfiguration-topic"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to which Amazon S3 publishes a message when it detects events of the specified type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-topicconfiguration--examples"></a>



### Receive S3 bucket notifications to an SNS topic<a name="aws-properties-s3-bucket-topicconfiguration--examples--Receive_S3_bucket_notifications_to_an_SNS_topic"></a>

The following example template shows an Amazon S3 bucket with a notification configuration that sends an event to the specified SNS topic when S3 has lost all replicas of an object\.

#### JSON<a name="aws-properties-s3-bucket-topicconfiguration--examples--Receive_S3_bucket_notifications_to_an_SNS_topic--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "Private",
                "NotificationConfiguration": {
                    "TopicConfigurations": [
                        {
                            "Topic": "arn:aws:sns:us-east-1:123456789012:TestTopic",
                            "Event": "s3:ReducedRedundancyLostObject"
                        }
                    ]
                }
            }
        }
    },
    "Outputs": {
        "BucketName": {
            "Value": {
                "Ref": "S3Bucket"
            },
            "Description": "Name of the sample Amazon S3 bucket with a notification configuration."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-topicconfiguration--examples--Receive_S3_bucket_notifications_to_an_SNS_topic--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: Private
      NotificationConfiguration:
        TopicConfigurations:
          - Topic: 'arn:aws:sns:us-east-1:123456789012:TestTopic'
            Event: 's3:ReducedRedundancyLostObject'
Outputs:
  BucketName:
    Value: !Ref S3Bucket
    Description: Name of the sample Amazon S3 bucket with a notification configuration.
```