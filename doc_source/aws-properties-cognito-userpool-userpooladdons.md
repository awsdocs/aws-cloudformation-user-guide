# AWS::Cognito::UserPool UserPoolAddOns<a name="aws-properties-cognito-userpool-userpooladdons"></a>

`UserPoolAddOns` is a property of the [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html) resource that enables advanced security risk detection\.

## Syntax<a name="aws-properties-cognito-userpool-userpooladdons-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-userpooladdons-syntax.json"></a>

```
{
  "[AdvancedSecurityMode](#cfn-cognito-userpool-userpooladdons-advancedsecuritymode)" : String
}
```

### YAML<a name="aws-properties-cognito-userpool-userpooladdons-syntax.yaml"></a>

```
  [AdvancedSecurityMode](#cfn-cognito-userpool-userpooladdons-advancedsecuritymode): String
```

## Properties<a name="aws-properties-cognito-userpool-userpooladdons-properties"></a>

`AdvancedSecurityMode`  <a name="cfn-cognito-userpool-userpooladdons-advancedsecuritymode"></a>
The advanced security mode\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `AUDIT | ENFORCED | OFF`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)