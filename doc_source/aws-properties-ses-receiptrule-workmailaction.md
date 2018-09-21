# Amazon Simple Email Service ReceiptRule WorkmailAction<a name="aws-properties-ses-receiptrule-workmailaction"></a>

<a name="aws-properties-ses-receiptrule-workmailaction-description"></a>The `WorkmailAction` property type includes an action in an Amazon SES receipt rule that calls Amazon WorkMail and, optionally, publishes a notification to Amazon SNS\.

You will typically not use this action directly because Amazon WorkMail adds the rule automatically during its setup procedure\.

For information using a receipt rule to call Amazon WorkMail, see [WorkMail Action](url-ses-dev;receiving-email-action-workmail.html) in the *Amazon Simple Email Service Developer Guide*\.

<a name="aws-properties-ses-receiptrule-workmailaction-inheritance"></a> `WorkmailAction` is a property of the [Amazon Simple Email Service ReceiptRule Action](aws-properties-ses-receiptrule-action.md) property type\.

## Syntax<a name="aws-properties-ses-receiptrule-workmailaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-receiptrule-workmailaction-syntax.json"></a>

```
{
  "[TopicArn](#cfn-ses-receiptrule-workmailaction-topicarn)" : String,
  "[OrganizationArn](#cfn-ses-receiptrule-workmailaction-organizationarn)" : String
}
```

### YAML<a name="aws-properties-ses-receiptrule-workmailaction-syntax.yaml"></a>

```
[TopicArn](#cfn-ses-receiptrule-workmailaction-topicarn): String
[OrganizationArn](#cfn-ses-receiptrule-workmailaction-organizationarn): String
```

## Properties<a name="aws-properties-ses-receiptrule-workmailaction-properties"></a>

`OrganizationArn`  <a name="cfn-ses-receiptrule-workmailaction-organizationarn"></a>
The ARN of the Amazon WorkMail organization\. An example of an Amazon WorkMail organization ARN is `arn:aws:workmail:us-west-2:123456789012:organization/m-68755160c4cb4e29a2b2f8fb58f359d7`\. For information about Amazon WorkMail organizations, see [Working with Organizations](url-wm-admin;organizations_overview.html) in the *Amazon WorkMail Administrator Guide*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TopicArn`  <a name="cfn-ses-receiptrule-workmailaction-topicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon SNS topic to notify when the WorkMail action is called\. An example of an Amazon SNS topic ARN is `arn:aws:sns:us-west-2:123456789012:MyTopic`\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ses-receiptrule-workmailaction-seealso"></a>
+ [Creating Receipt Rules for Amazon SES Email Receiving](url-ses-dev;receiving-email-receipt-rules.html) in the *Amazon Simple Email Service Developer Guide*
+ [WorkMail Action](url-ses-dev;receiving-email-action-workmail.html) in the *Amazon Simple Email Service Developer Guide*
+ [WorkmailAction](url-ses-api;API_WorkmailAction.html) in the *Amazon Simple Email Service API Reference*