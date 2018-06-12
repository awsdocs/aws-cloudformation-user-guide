# Amazon Simple Storage Service Bucket TopicConfiguration<a name="aws-properties-s3-bucket-notificationconfig-topicconfig"></a>

Describes the topic and events for the [Amazon S3 Bucket NotificationConfiguration](aws-properties-s3-bucket-notificationconfig.md) property\.

## Syntax<a name="w3ab2c21c14e1792b5"></a>

### JSON<a name="aws-properties-s3-bucket-notificationconfig-topicconfig-syntax.json"></a>

```
{
  "[Event](#cfn-s3-bucket-notificationconfig-topicconfig-event)" : String,
  "[Filter](#cfn-s3-bucket-notificationconfig-topicconfig-filter)" : Filter,
  "[Topic](#cfn-s3-bucket-notificationconfig-topicconfig-topic)" : String 
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfig-topicconfig-syntax.yaml"></a>

```
[Event](#cfn-s3-bucket-notificationconfig-topicconfig-event): String
[Filter](#cfn-s3-bucket-notificationconfig-topicconfig-filter):
  Filter
[Topic](#cfn-s3-bucket-notificationconfig-topicconfig-topic): String
```

## Properties<a name="w3ab2c21c14e1792b7"></a>

`Event`  <a name="cfn-s3-bucket-notificationconfig-topicconfig-event"></a>
The Amazon Simple Storage Service \(Amazon S3\) bucket event about which to send notifications\. For more information, see [Supported Event Types](http://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: String

`Filter`  <a name="cfn-s3-bucket-notificationconfig-topicconfig-filter"></a>
The filtering rules that determine for which objects to send notifications\. For example, you can create a filter so that Amazon Simple Storage Service \(Amazon S3\) sends notifications only when image files with a `.jpg` extension are added to the bucket\.  
*Required*: No  
*Type*: [Amazon S3 Bucket NotificationFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter.md)

`Topic`  <a name="cfn-s3-bucket-notificationconfig-topicconfig-topic"></a>
The Amazon SNS topic Amazon Resource Name \(ARN\) to which Amazon S3 reports the specified events\.  
*Required*: Yes  
*Type*: String