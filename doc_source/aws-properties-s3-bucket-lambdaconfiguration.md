# AWS::S3::Bucket LambdaConfiguration<a name="aws-properties-s3-bucket-lambdaconfiguration"></a>

Describes the AWS Lambda functions to invoke and the events for which to invoke them\.

## Syntax<a name="aws-properties-s3-bucket-lambdaconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-lambdaconfiguration-syntax.json"></a>

```
{
  "[Event](#cfn-s3-bucket-lambdaconfiguration-event)" : String,
  "[Filter](#cfn-s3-bucket-lambdaconfiguration-filter)" : NotificationFilter,
  "[Function](#cfn-s3-bucket-lambdaconfiguration-function)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-lambdaconfiguration-syntax.yaml"></a>

```
  [Event](#cfn-s3-bucket-lambdaconfiguration-event): String
  [Filter](#cfn-s3-bucket-lambdaconfiguration-filter): 
    NotificationFilter
  [Function](#cfn-s3-bucket-lambdaconfiguration-function): String
```

## Properties<a name="aws-properties-s3-bucket-lambdaconfiguration-properties"></a>

`Event`  <a name="cfn-s3-bucket-lambdaconfiguration-event"></a>
The Amazon S3 bucket event for which to invoke the AWS Lambda function\. For more information, see [Supported Event Types](https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html) in the *Amazon S3 User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-s3-bucket-lambdaconfiguration-filter"></a>
The filtering rules that determine which objects invoke the AWS Lambda function\. For example, you can create a filter so that only image files with a `.jpg` extension invoke the function when they are added to the Amazon S3 bucket\.  
*Required*: No  
*Type*: [NotificationFilter](aws-properties-s3-bucket-notificationfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Function`  <a name="cfn-s3-bucket-lambdaconfiguration-function"></a>
The Amazon Resource Name \(ARN\) of the AWS Lambda function that Amazon S3 invokes when the specified event type occurs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)