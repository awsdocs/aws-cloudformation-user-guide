# AWS::Cognito::UserPoolRiskConfigurationAttachment NotifyEmailType<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype"></a>

The notify email type\.

## Syntax<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype-syntax.json"></a>

```
{
  "[HtmlBody](#cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-htmlbody)" : String,
  "[Subject](#cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-subject)" : String,
  "[TextBody](#cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-textbody)" : String
}
```

### YAML<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype-syntax.yaml"></a>

```
  [HtmlBody](#cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-htmlbody): String
  [Subject](#cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-subject): String
  [TextBody](#cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-textbody): String
```

## Properties<a name="aws-properties-cognito-userpoolriskconfigurationattachment-notifyemailtype-properties"></a>

`HtmlBody`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-htmlbody"></a>
The HTML body\.  
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `20000`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subject`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-subject"></a>
The subject\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextBody`  <a name="cfn-cognito-userpoolriskconfigurationattachment-notifyemailtype-textbody"></a>
The text body\.  
*Required*: No  
*Type*: String  
*Minimum*: `6`  
*Maximum*: `20000`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}\s*]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)