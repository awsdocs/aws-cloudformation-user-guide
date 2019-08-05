# AWS::Cognito::UserPool SmsConfiguration<a name="aws-properties-cognito-userpool-smsconfiguration"></a>

`SmsConfiguration` is a property of the [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html) resource that defines the SMS configuration of an Amazon Cognito User Pool\.

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
The external ID used in IAM role trust relationships\.
For more information about using external IDs, see [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html) in the *AWS Identity and Access Management User Guide*\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsCallerArn`  <a name="cfn-cognito-userpool-smsconfiguration-snscallerarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service \(SNS\) caller\.
*Required*: No
*Type*: String
*Minimum*: `20`
*Maximum*: `2048`
*Pattern*: `arn:[\w+=/,.@-]+:[\w+=/,.@-]+:([\w+=/,.@-]*)?:[0-9]+:[\w+=/,.@-]+(:[\w+=/,.@-]+)?(:[\w+=/,.@-]+)?`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
