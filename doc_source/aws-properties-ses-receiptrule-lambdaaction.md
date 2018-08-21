# Amazon Simple Email Service ReceiptRule LambdaAction<a name="aws-properties-ses-receiptrule-lambdaaction"></a>

<a name="aws-properties-ses-receiptrule-lambdaaction-description"></a>The `LambdaAction` property type includes an action in an Amazon SES receipt rule that calls an AWS Lambda function and, optionally, publishes a notification to Amazon SNS\.

To enable Amazon SES to call your AWS Lambda function or to publish to an Amazon SNS topic of another account, Amazon SES must have permission to access those resources\. For information about giving permissions, see [Giving Permissions to Amazon SES for Email Receiving](url-ses-dev;receiving-email-permissions.html) in the *Amazon Simple Email Service Developer Guide*\. For information about using AWS Lambda actions in receipt rules, see [Lambda Action](url-ses-dev;receiving-email-action-lambda.html) in the *Amazon Simple Email Service Developer Guide*\.

<a name="aws-properties-ses-receiptrule-lambdaaction-inheritance"></a> `LambdaAction` is a property of the [Amazon Simple Email Service ReceiptRule Action](aws-properties-ses-receiptrule-action.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-lambdaaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-lambdaaction-syntax.json"></a>

```
{
  "[FunctionArn](#cfn-ses-receiptrule-lambdaaction-functionarn)" : String,
  "[TopicArn](#cfn-ses-receiptrule-lambdaaction-topicarn)" : String,
  "[InvocationType](#cfn-ses-receiptrule-lambdaaction-invocationtype)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-lambdaaction-syntax.yaml"></a>

```
[FunctionArn](#cfn-ses-receiptrule-lambdaaction-functionarn): String
[TopicArn](#cfn-ses-receiptrule-lambdaaction-topicarn): String
[InvocationType](#cfn-ses-receiptrule-lambdaaction-invocationtype): String
```

## Properties<a name="aws-properties-ses-receiptrule-lambdaaction-properties"></a>

`FunctionArn`  <a name="cfn-ses-receiptrule-lambdaaction-functionarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Lambda function\. An example of an AWS Lambda function ARN is `arn:aws:lambda:us-west-2:account-id:function:MyFunction`\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InvocationType`  <a name="cfn-ses-receiptrule-lambdaaction-invocationtype"></a>
The invocation type of the AWS Lambda function\. An invocation type of `RequestResponse` means that the execution of the function will immediately result in a response, and a value of `Event` means that the function will be invoked asynchronously\. The default value is `Event`\. For information about AWS Lambda invocation types, see [Creating Receipt Rules for Amazon SES Email Receiving](url-lam-dev;API_Invoke.html) in the *AWS Lambda Developer Guide*\.  
Valid values include `Event` and `RequestResponse`\.  
There is a 30\-second timeout on `RequestResponse` invocations\. You should use `Event` invocation in most cases\. Use `RequestResponse` only when you want to make a mail flow decision, such as whether to stop the receipt rule or the receipt rule set\. 
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TopicArn`  <a name="cfn-ses-receiptrule-lambdaaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the Lambda action is taken\. An example of an Amazon SNS topic ARN is `arn:aws:sns:us-west-2:123456789012:MyTopic`\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-lambdaaction-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [Giving Permissions to Amazon SES for Email Receiving](url-ses-dev;receiving-email-permissions.html) in the *Amazon Simple Email Service Developer Guide*
+ [Lambda Action](url-ses-dev;receiving-email-action-lambda.html) in the *Amazon Simple Email Service Developer Guide*
+ [LambdaAction](url-ses-api;API_LambdaAction.html) in the *Amazon Simple Email Service API Reference*