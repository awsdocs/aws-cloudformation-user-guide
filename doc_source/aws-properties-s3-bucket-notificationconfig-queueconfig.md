# AWS::S3::Bucket QueueConfiguration<a name="aws-properties-s3-bucket-notificationconfig-queueconfig"></a>

Specifies the configuration for publishing messages to an Amazon Simple Queue Service \(Amazon SQS\) queue when Amazon S3 detects specified events\.

## Syntax<a name="aws-properties-s3-bucket-notificationconfig-queueconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-notificationconfig-queueconfig-syntax.json"></a>

```
{
  "[Event](#cfn-s3-bucket-notificationconfig-queueconfig-event)" : String,
  "[Filter](#cfn-s3-bucket-notificationconfig-queueconfig-filter)" : NotificationFilter,
  "[Queue](#cfn-s3-bucket-notificationconfig-queueconfig-queue)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfig-queueconfig-syntax.yaml"></a>

```
  [Event](#cfn-s3-bucket-notificationconfig-queueconfig-event): String
  [Filter](#cfn-s3-bucket-notificationconfig-queueconfig-filter): 
    NotificationFilter
  [Queue](#cfn-s3-bucket-notificationconfig-queueconfig-queue): String
```

## Properties<a name="aws-properties-s3-bucket-notificationconfig-queueconfig-properties"></a>

`Event`  <a name="cfn-s3-bucket-notificationconfig-queueconfig-event"></a>
The Amazon S3 bucket event about which you want to publish messages to Amazon SQS\. For more information, see [Supported Event Types](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-s3-bucket-notificationconfig-queueconfig-filter"></a>
 The filtering rules that determine which objects trigger notifications\. For example, you can create a filter so that Amazon S3 sends notifications only when image files with a `.jpg` extension are added to the bucket\.   
*Required*: No  
*Type*: [NotificationFilter](aws-properties-s3-bucket-notificationconfiguration-config-filter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Queue`  <a name="cfn-s3-bucket-notificationconfig-queueconfig-queue"></a>
The Amazon Resource Name \(ARN\) of the Amazon SQS queue to which Amazon S3 publishes a message when it detects events of the specified type\. FIFO queues are not allowed when enabling an SQS queue as the event notification destination\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)