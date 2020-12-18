# AWS::S3::Bucket TopicConfiguration<a name="aws-properties-s3-bucket-notificationconfig-topicconfig"></a>

A container for specifying the configuration for publication of messages to an Amazon Simple Notification Service \(Amazon SNS\) topic when Amazon S3 detects specified events\.

## Syntax<a name="aws-properties-s3-bucket-notificationconfig-topicconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-notificationconfig-topicconfig-syntax.json"></a>

```
{
  "[Event](#cfn-s3-bucket-notificationconfig-topicconfig-event)" : String,
  "[Filter](#cfn-s3-bucket-notificationconfig-topicconfig-filter)" : NotificationFilter,
  "[Topic](#cfn-s3-bucket-notificationconfig-topicconfig-topic)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfig-topicconfig-syntax.yaml"></a>

```
  [Event](#cfn-s3-bucket-notificationconfig-topicconfig-event): String
  [Filter](#cfn-s3-bucket-notificationconfig-topicconfig-filter): 
    NotificationFilter
  [Topic](#cfn-s3-bucket-notificationconfig-topicconfig-topic): String
```

## Properties<a name="aws-properties-s3-bucket-notificationconfig-topicconfig-properties"></a>

`Event`  <a name="cfn-s3-bucket-notificationconfig-topicconfig-event"></a>
The Amazon S3 bucket event about which to send notifications\. For more information, see [Supported Event Types](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-s3-bucket-notificationconfig-topicconfig-filter"></a>
The filtering rules that determine for which objects to send notifications\. For example, you can create a filter so that Amazon S3 sends notifications only when image files with a `.jpg` extension are added to the bucket\.  
*Required*: No  
*Type*: [NotificationFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Topic`  <a name="cfn-s3-bucket-notificationconfig-topicconfig-topic"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to which Amazon S3 publishes a message when it detects events of the specified type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-notificationconfig-topicconfig--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

