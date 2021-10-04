# AWS::SSMIncidents::ResponsePlan NotificationTargetItem<a name="aws-properties-ssmincidents-responseplan-notificationtargetitem"></a>

The SNS topic that's used by AWS Chatbot to notify the incidents chat channel\.

## Syntax<a name="aws-properties-ssmincidents-responseplan-notificationtargetitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmincidents-responseplan-notificationtargetitem-syntax.json"></a>

```
{
  "[SnsTopicArn](#cfn-ssmincidents-responseplan-notificationtargetitem-snstopicarn)" : String
}
```

### YAML<a name="aws-properties-ssmincidents-responseplan-notificationtargetitem-syntax.yaml"></a>

```
  [SnsTopicArn](#cfn-ssmincidents-responseplan-notificationtargetitem-snstopicarn): String
```

## Properties<a name="aws-properties-ssmincidents-responseplan-notificationtargetitem-properties"></a>

`SnsTopicArn`  <a name="cfn-ssmincidents-responseplan-notificationtargetitem-snstopicarn"></a>
The Amazon Resource Name \(ARN\) of the SNS topic\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000`  
*Pattern*: `^arn:aws(-cn|-us-gov)?:[a-z0-9-]*:[a-z0-9-]*:([0-9]{12})?:.+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)