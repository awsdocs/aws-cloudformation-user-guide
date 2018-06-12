# Amazon Cognito UserPool EmailConfiguration<a name="aws-properties-cognito-userpool-emailconfiguration"></a>

`EmailConfiguration` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the email configuration of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-emailconfiguration-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-emailconfiguration-syntax.json"></a>

```
{
  "[ReplyToEmailAddress](#cfn-cognito-userpool-emailconfiguration-replytoemailaddress)" : String,
  "[SourceArn](#cfn-cognito-userpool-emailconfiguration-sourcearn)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-emailconfiguration-syntax.yaml"></a>

```
[ReplyToEmailAddress](#cfn-cognito-userpool-emailconfiguration-replytoemailaddress): String
[SourceArn](#cfn-cognito-userpool-emailconfiguration-sourcearn): String
```

## Properties<a name="aws-properties-cognito-userpool-emailconfiguration-properties"></a>

`ReplyToEmailAddress`  <a name="cfn-cognito-userpool-emailconfiguration-replytoemailaddress"></a>
The REPLY\-TO email address\.  
*Type*: String  
*Required*: No

`SourceArn`  <a name="cfn-cognito-userpool-emailconfiguration-sourcearn"></a>
The Amazon Resource Name \(ARN\) of the email source\.  
*Type*: String  
*Required*: No