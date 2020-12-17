# AWS::S3::Bucket NotificationConfiguration<a name="aws-properties-s3-bucket-notificationconfig"></a>

Describes the notification configuration for an Amazon S3 bucket\.

**Note**  
If you create the target resource and related permissions in the same template, you might have a circular dependency\.  
For example, you might use the `AWS::Lambda::Permission` resource to grant the bucket permission to invoke an AWS Lambda function\. However, AWS CloudFormation can't create the bucket until the bucket has permission to invoke the function \(AWS CloudFormation checks whether the bucket can invoke the function\)\. If you're using Refs to pass the bucket name, this leads to a circular dependency\.  
To avoid this dependency, you can create all resources without specifying the notification configuration\. Then, update the stack with a notification configuration\.  
For more information on permissions, see [AWS::Lambda::Permission](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-permission.html) and [Granting Permissions to Publish Event Notification Messages to a Destination](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html#grant-destinations-permissions-to-s3)\.

## Syntax<a name="aws-properties-s3-bucket-notificationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-notificationconfig-syntax.json"></a>

```
{
  "[LambdaConfigurations](#cfn-s3-bucket-notificationconfig-lambdaconfig)" : [ LambdaConfiguration, ... ],
  "[QueueConfigurations](#cfn-s3-bucket-notificationconfig-queueconfig)" : [ QueueConfiguration, ... ],
  "[TopicConfigurations](#cfn-s3-bucket-notificationconfig-topicconfig)" : [ TopicConfiguration, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-notificationconfig-syntax.yaml"></a>

```
  [LambdaConfigurations](#cfn-s3-bucket-notificationconfig-lambdaconfig): 
    - LambdaConfiguration
  [QueueConfigurations](#cfn-s3-bucket-notificationconfig-queueconfig): 
    - QueueConfiguration
  [TopicConfigurations](#cfn-s3-bucket-notificationconfig-topicconfig): 
    - TopicConfiguration
```

## Properties<a name="aws-properties-s3-bucket-notificationconfig-properties"></a>

`LambdaConfigurations`  <a name="cfn-s3-bucket-notificationconfig-lambdaconfig"></a>
Describes the AWS Lambda functions to invoke and the events for which to invoke them\.  
*Required*: No  
*Type*: List of [LambdaConfiguration](aws-properties-s3-bucket-notificationconfig-lambdaconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueConfigurations`  <a name="cfn-s3-bucket-notificationconfig-queueconfig"></a>
The Amazon Simple Queue Service queues to publish messages to and the events for which to publish messages\.  
*Required*: No  
*Type*: List of [QueueConfiguration](aws-properties-s3-bucket-notificationconfig-queueconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicConfigurations`  <a name="cfn-s3-bucket-notificationconfig-topicconfig"></a>
The topic to which notifications are sent and the events for which notifications are generated\.  
*Required*: No  
*Type*: List of [TopicConfiguration](aws-properties-s3-bucket-notificationconfig-topicconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-notificationconfig--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

