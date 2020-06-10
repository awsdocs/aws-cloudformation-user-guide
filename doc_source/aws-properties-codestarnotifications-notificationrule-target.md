# AWS::CodeStarNotifications::NotificationRule Target<a name="aws-properties-codestarnotifications-notificationrule-target"></a>

Information about the SNS topics or AWS Chatbot clients associated with a notification rule\.

## Syntax<a name="aws-properties-codestarnotifications-notificationrule-target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codestarnotifications-notificationrule-target-syntax.json"></a>

```
{
  "[TargetAddress](#cfn-codestarnotifications-notificationrule-target-targetaddress)" : String,
  "[TargetType](#cfn-codestarnotifications-notificationrule-target-targettype)" : String
}
```

### YAML<a name="aws-properties-codestarnotifications-notificationrule-target-syntax.yaml"></a>

```
  [TargetAddress](#cfn-codestarnotifications-notificationrule-target-targetaddress): String
  [TargetType](#cfn-codestarnotifications-notificationrule-target-targettype): String
```

## Properties<a name="aws-properties-codestarnotifications-notificationrule-target-properties"></a>

`TargetAddress`  <a name="cfn-codestarnotifications-notificationrule-target-targetaddress"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic or AWS Chatbot client\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `320`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetType`  <a name="cfn-codestarnotifications-notificationrule-target-targettype"></a>
The target type\. Can be an Amazon SNS topic or AWS Chatbot client\.  
+ Amazon SNS topics are specified as `SNS`\.
+ AWS Chatbot clients are specified as `AWSChatbotSlack`\.
*Required*: No  
*Type*: String  
*Pattern*: `^[A-Za-z]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)