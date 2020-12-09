# AWS::Cognito::UserPool SmsConfiguration<a name="aws-properties-cognito-userpool-smsconfiguration"></a>

The SMS configuration type that includes the settings the Cognito User Pool needs to call for the Amazon SNS service to send an SMS message from your AWS account\. The Cognito User Pool makes the request to the Amazon SNS Service by using an AWS IAM role that you provide for your AWS account\.

## Syntax<a name="aws-properties-cognito-userpool-smsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-smsconfiguration-syntax.json"></a>

```
{
  "[ExternalId](#cfn-cognito-userpool-smsconfiguration-externalid)" : String,
  "[SnsCallerArn](#cfn-cognito-userpool-smsconfiguration-snscallerarn)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-smsconfiguration-syntax.yaml"></a>

```
  [ExternalId](#cfn-cognito-userpool-smsconfiguration-externalid): String
  [SnsCallerArn](#cfn-cognito-userpool-smsconfiguration-snscallerarn): String
```

## Properties<a name="aws-properties-cognito-userpool-smsconfiguration-properties"></a>

`ExternalId`  <a name="cfn-cognito-userpool-smsconfiguration-externalid"></a>
The external ID is a value\. We recommend you use `ExternalId`to add security to your IAM role, which is used to call Amazon SNS to send SMS messages for your user pool\. If you provide an `ExternalId`, the Cognito User Pool uses it when attempting to assume your IAM role\. You can also set your roles trust policy to require the `ExternalID`\. If you use the Cognito Management Console to create a role for SMS MFA, Cognito creates a role with the required permissions and a trust policy that uses `ExternalId`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsCallerArn`  <a name="cfn-cognito-userpool-smsconfiguration-snscallerarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service \(SNS\) caller\. This is the ARN of the IAM role in your AWS account which Cognito will use to send SMS messages\. SMS messages are subject to a [spending limit](https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-email-phone-verification.html)\.   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)