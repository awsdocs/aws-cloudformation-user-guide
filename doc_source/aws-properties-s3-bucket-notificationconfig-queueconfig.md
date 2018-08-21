# Amazon Simple Storage Service Bucket QueueConfiguration<a name="aws-properties-s3-bucket-notificationconfig-queueconfig"></a>

`QueueConfigurations` is a property of the [Amazon S3 Bucket NotificationConfiguration](aws-properties-s3-bucket-notificationconfig.md) property that describes the S3 bucket events about which you want to send messages to Amazon SQS and the queues to which you want to send them\.

## Syntax<a name="w3ab2c21c14e1748b5"></a>

### JSON<a name="aws-properties-s3-bucket-notificationconfig-queueconfig-syntax.json"></a>

```
{
  "[Event](#cfn-s3-bucket-notificationconfig-queueconfig-event)" : String,
  "[Filter](#cfn-s3-bucket-notificationconfig-queueconfig-filter)" : Filter,
  "[Queue](#cfn-s3-bucket-notificationconfig-queueconfig-queue)" : String 
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfig-queueconfig-syntax.yaml"></a>

```
[Event](#cfn-s3-bucket-notificationconfig-queueconfig-event): String
[Filter](#cfn-s3-bucket-notificationconfig-queueconfig-filter):
  Filter
[Queue](#cfn-s3-bucket-notificationconfig-queueconfig-queue): String
```

## Properties<a name="w3ab2c21c14e1748b7"></a>

`Event`  <a name="cfn-s3-bucket-notificationconfig-queueconfig-event"></a>
The S3 bucket event about which you want to publish messages to Amazon Simple Queue Service \( Amazon SQS\)\. For more information, see [Supported Event Types](http://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: String

`Filter`  <a name="cfn-s3-bucket-notificationconfig-queueconfig-filter"></a>
The filtering rules that determine for which objects to send notifications\. For example, you can create a filter so that Amazon Simple Storage Service \(Amazon S3\) sends notifications only when image files with a `.jpg` extension are added to the bucket\.  
*Required*: No  
*Type*: [Amazon S3 Bucket NotificationFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter.md)

`Queue`  <a name="cfn-s3-bucket-notificationconfig-queueconfig-queue"></a>
The Amazon Resource Name \(ARN\) of the Amazon SQS queue that Amazon S3 publishes messages to when the specified event type occurs\.  
*Required*: Yes  
*Type*: String