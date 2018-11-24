# Amazon Cognito UserPool SmsConfiguration<a name="aws-properties-cognito-userpool-smsconfiguration"></a>

`SmsConfiguration` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the SMS configuration of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-smsconfiguration-syntax"></a>

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
For more information about using external IDs, see [How to Use an External ID When Granting Access to Your AWS Resources to a Third Party](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-user_externalid.html) in the *AWS Identity and Access Management User Guide*\.  
*Type*: String  
*Required*: No

`SnsCallerArn`  <a name="cfn-cognito-userpool-smsconfiguration-snscallerarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service \(SNS\) caller\.  
*Type*: String  
*Required*: Yes