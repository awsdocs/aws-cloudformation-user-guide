# AWS::SageMaker::Workteam NotificationConfiguration<a name="aws-properties-sagemaker-workteam-notificationconfiguration"></a>

Configures Amazon SNS notifications of available or expiring work items for work teams\.

## Syntax<a name="aws-properties-sagemaker-workteam-notificationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-workteam-notificationconfiguration-syntax.json"></a>

```
{
  "[NotificationTopicArn](#cfn-sagemaker-workteam-notificationconfiguration-notificationtopicarn)" : String
}
```

### YAML<a name="aws-properties-sagemaker-workteam-notificationconfiguration-syntax.yaml"></a>

```
  [NotificationTopicArn](#cfn-sagemaker-workteam-notificationconfiguration-notificationtopicarn): String
```

## Properties<a name="aws-properties-sagemaker-workteam-notificationconfiguration-properties"></a>

`NotificationTopicArn`  <a name="cfn-sagemaker-workteam-notificationconfiguration-notificationtopicarn"></a>
The ARN for the Amazon SNS topic to which notifications should be published\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `arn:aws[a-z\-]*:sns:[a-z0-9\-]*:[0-9]{12}:[a-zA-Z0-9_.-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)