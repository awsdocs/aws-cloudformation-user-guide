# Amazon Simple Email Service ReceiptRule StopAction<a name="aws-properties-ses-receiptrule-stopaction"></a>

<a name="aws-properties-ses-receiptrule-stopaction-description"></a>The `StopAction` property type includes an action in an Amazon SES receipt rule that terminates the evaluation of the receipt rule set and, optionally, publishes a notification to Amazon SNS\.

<a name="aws-properties-ses-receiptrule-stopaction-inheritance"></a> `StopAction` is a property of the [Amazon Simple Email Service ReceiptRule Action](aws-properties-ses-receiptrule-action.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-stopaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-stopaction-syntax.json"></a>

```
{
  "[Scope](#cfn-ses-receiptrule-stopaction-scope)" : String,
  "[TopicArn](#cfn-ses-receiptrule-stopaction-topicarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-stopaction-syntax.yaml"></a>

```
[Scope](#cfn-ses-receiptrule-stopaction-scope): String
[TopicArn](#cfn-ses-receiptrule-stopaction-topicarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-stopaction-properties"></a>

`Scope`  <a name="cfn-ses-receiptrule-stopaction-scope"></a>
The name of the RuleSet that is being stopped\.   
Valid values include: `RuleSet`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TopicArn`  <a name="cfn-ses-receiptrule-stopaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the stop action is taken\. An example of an Amazon SNS topic ARN is `arn:aws:sns:us-west-2:123456789012:MyTopic`\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-stopaction-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [StopAction](url-ses-api;API_StopAction.html) in the *Amazon Simple Email Service API Reference*