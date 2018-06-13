# Amazon Simple Email Service ReceiptRule Action<a name="aws-properties-ses-receiptrule-action"></a>

<a name="aws-properties-ses-receiptrule-action-description"></a>The `Action` property type specifies an action for Amazon SES to take when it receives an email on behalf of one or more email addresses or domains that you own\.

<a name="aws-properties-ses-receiptrule-action-inheritance"></a> `Action` is a property of the [Amazon Simple Email Service ReceiptRule Rule](aws-properties-ses-receiptrule-rule.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-action-syntax.json"></a>

```
{
  "[BounceAction](#cfn-ses-receiptrule-action-bounceaction)" : [*BounceAction*](aws-properties-ses-receiptrule-bounceaction.md),
  "[S3Action](#cfn-ses-receiptrule-action-s3action)" : [*S3Action*](aws-properties-ses-receiptrule-s3action.md),
  "[StopAction](#cfn-ses-receiptrule-action-stopaction)" : [*StopAction*](aws-properties-ses-receiptrule-stopaction.md),
  "[SNSAction](#cfn-ses-receiptrule-action-snsaction)" : [*SNSAction*](aws-properties-ses-receiptrule-snsaction.md),
  "[WorkmailAction](#cfn-ses-receiptrule-action-workmailaction)" : [*WorkmailAction*](aws-properties-ses-receiptrule-workmailaction.md),
  "[AddHeaderAction](#cfn-ses-receiptrule-action-addheaderaction)" : [*AddHeaderAction*](aws-properties-ses-receiptrule-addheaderaction.md),
  "[LambdaAction](#cfn-ses-receiptrule-action-lambdaaction)" : [*LambdaAction*](aws-properties-ses-receiptrule-lambdaaction.md)
}
```

### YAML<a name="aws-properties-ses-receiptrule-action-syntax.yaml"></a>

```
[BounceAction](#cfn-ses-receiptrule-action-bounceaction): [*BounceAction*](aws-properties-ses-receiptrule-bounceaction.md)
[S3Action](#cfn-ses-receiptrule-action-s3action): [*S3Action*](aws-properties-ses-receiptrule-s3action.md)
[StopAction](#cfn-ses-receiptrule-action-stopaction): [*StopAction*](aws-properties-ses-receiptrule-stopaction.md)
[SNSAction](#cfn-ses-receiptrule-action-snsaction): [*SNSAction*](aws-properties-ses-receiptrule-snsaction.md)
[WorkmailAction](#cfn-ses-receiptrule-action-workmailaction): [*WorkmailAction*](aws-properties-ses-receiptrule-workmailaction.md)
[AddHeaderAction](#cfn-ses-receiptrule-action-addheaderaction): [*AddHeaderAction*](aws-properties-ses-receiptrule-addheaderaction.md)
[LambdaAction](#cfn-ses-receiptrule-action-lambdaaction): [*LambdaAction*](aws-properties-ses-receiptrule-lambdaaction.md)
```

## Properties<a name="aws-properties-ses-receiptrule-action-properties"></a>

`AddHeaderAction`  <a name="cfn-ses-receiptrule-action-addheaderaction"></a>
Adds a header to the received email\.  
 *Required*: No  
 *Type*: [Amazon SES ReceiptRule AddHeaderAction](aws-properties-ses-receiptrule-addheaderaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`BounceAction`  <a name="cfn-ses-receiptrule-action-bounceaction"></a>
Rejects the received email by returning a bounce response to the sender and, optionally, publishes a notification to Amazon SNS\.  
 *Required*: No  
 *Type*: [Amazon SES ReceiptRule BounceAction](aws-properties-ses-receiptrule-bounceaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LambdaAction`  <a name="cfn-ses-receiptrule-action-lambdaaction"></a>
Calls an AWS Lambda function, and optionally, publishes a notification to Amazon SNS\.  
 *Required*: No  
 *Type*: [Amazon SES ReceiptRule LambdaAction](aws-properties-ses-receiptrule-lambdaaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Action`  <a name="cfn-ses-receiptrule-action-s3action"></a>
Saves the received message to an Amazon S3 bucket and, optionally, publishes a notification to Amazon SNS\.  
 *Required*: No  
 *Type*: [Amazon SES ReceiptRule S3Action](aws-properties-ses-receiptrule-s3action.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SNSAction`  <a name="cfn-ses-receiptrule-action-snsaction"></a>
Publishes the email content within a notification to Amazon SNS\.  
 *Required*: No  
 *Type*: [Amazon SES ReceiptRule SNSAction](aws-properties-ses-receiptrule-snsaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`StopAction`  <a name="cfn-ses-receiptrule-action-stopaction"></a>
Terminates the evaluation of the receipt rule set and optionally publishes a notification to Amazon SNS\.  
 *Required*: No  
 *Type*: [Amazon SES ReceiptRule StopAction](aws-properties-ses-receiptrule-stopaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`WorkmailAction`  <a name="cfn-ses-receiptrule-action-workmailaction"></a>
Calls Amazon WorkMail and, optionally, publishes a notification to Amazon SNS\.  
 *Required*: No  
 *Type*: [Amazon SES ReceiptRule WorkmailAction](aws-properties-ses-receiptrule-workmailaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-action-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [CreateReceiptRule](url-ses-api;API_CreateReceiptRule.html) in the *Amazon Simple Email Service API Reference*
+ [ReceiptAction](url-ses-api;API_ReceiptAction.html) in the *Amazon Simple Email Service API Reference*