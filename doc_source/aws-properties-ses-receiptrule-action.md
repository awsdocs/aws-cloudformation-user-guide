# AWS::SES::ReceiptRule Action<a name="aws-properties-ses-receiptrule-action"></a>

An action that Amazon SES can take when it receives an email on behalf of one or more email addresses or domains that you own\. An instance of this data type can represent only one action\.

For information about setting up receipt rules, see the [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/receiving-email-receipt-rules.html)\.

## Syntax<a name="aws-properties-ses-receiptrule-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-action-syntax.json"></a>

```
{
  "[AddHeaderAction](#cfn-ses-receiptrule-action-addheaderaction)" : AddHeaderAction,
  "[BounceAction](#cfn-ses-receiptrule-action-bounceaction)" : BounceAction,
  "[LambdaAction](#cfn-ses-receiptrule-action-lambdaaction)" : LambdaAction,
  "[S3Action](#cfn-ses-receiptrule-action-s3action)" : S3Action,
  "[SNSAction](#cfn-ses-receiptrule-action-snsaction)" : SNSAction,
  "[StopAction](#cfn-ses-receiptrule-action-stopaction)" : StopAction,
  "[WorkmailAction](#cfn-ses-receiptrule-action-workmailaction)" : WorkmailAction
}
```

### YAML<a name="aws-properties-ses-receiptrule-action-syntax.yaml"></a>

```
  [AddHeaderAction](#cfn-ses-receiptrule-action-addheaderaction): 
    AddHeaderAction
  [BounceAction](#cfn-ses-receiptrule-action-bounceaction): 
    BounceAction
  [LambdaAction](#cfn-ses-receiptrule-action-lambdaaction): 
    LambdaAction
  [S3Action](#cfn-ses-receiptrule-action-s3action): 
    S3Action
  [SNSAction](#cfn-ses-receiptrule-action-snsaction): 
    SNSAction
  [StopAction](#cfn-ses-receiptrule-action-stopaction): 
    StopAction
  [WorkmailAction](#cfn-ses-receiptrule-action-workmailaction): 
    WorkmailAction
```

## Properties<a name="aws-properties-ses-receiptrule-action-properties"></a>

`AddHeaderAction`  <a name="cfn-ses-receiptrule-action-addheaderaction"></a>
Adds a header to the received email\.  
*Required*: No  
*Type*: [AddHeaderAction](aws-properties-ses-receiptrule-addheaderaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BounceAction`  <a name="cfn-ses-receiptrule-action-bounceaction"></a>
Rejects the received email by returning a bounce response to the sender and, optionally, publishes a notification to Amazon Simple Notification Service \(Amazon SNS\)\.  
*Required*: No  
*Type*: [BounceAction](aws-properties-ses-receiptrule-bounceaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaAction`  <a name="cfn-ses-receiptrule-action-lambdaaction"></a>
Calls an AWS Lambda function, and optionally, publishes a notification to Amazon SNS\.  
*Required*: No  
*Type*: [LambdaAction](aws-properties-ses-receiptrule-lambdaaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Action`  <a name="cfn-ses-receiptrule-action-s3action"></a>
Saves the received message to an Amazon Simple Storage Service \(Amazon S3\) bucket and, optionally, publishes a notification to Amazon SNS\.  
*Required*: No  
*Type*: [S3Action](aws-properties-ses-receiptrule-s3action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SNSAction`  <a name="cfn-ses-receiptrule-action-snsaction"></a>
Publishes the email content within a notification to Amazon SNS\.  
*Required*: No  
*Type*: [SNSAction](aws-properties-ses-receiptrule-snsaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StopAction`  <a name="cfn-ses-receiptrule-action-stopaction"></a>
Terminates the evaluation of the receipt rule set and optionally publishes a notification to Amazon SNS\.  
*Required*: No  
*Type*: [StopAction](aws-properties-ses-receiptrule-stopaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkmailAction`  <a name="cfn-ses-receiptrule-action-workmailaction"></a>
Calls Amazon WorkMail and, optionally, publishes a notification to Amazon SNS\.  
*Required*: No  
*Type*: [WorkmailAction](aws-properties-ses-receiptrule-workmailaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)