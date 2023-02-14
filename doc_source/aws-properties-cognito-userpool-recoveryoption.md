# AWS::Cognito::UserPool RecoveryOption<a name="aws-properties-cognito-userpool-recoveryoption"></a>

A map containing a priority as a key, and recovery method name as a value\.

## Syntax<a name="aws-properties-cognito-userpool-recoveryoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-recoveryoption-syntax.json"></a>

```
{
  "[Name](#cfn-cognito-userpool-recoveryoption-name)" : String,
  "[Priority](#cfn-cognito-userpool-recoveryoption-priority)" : Integer
}
```

### YAML<a name="aws-properties-cognito-userpool-recoveryoption-syntax.yaml"></a>

```
  [Name](#cfn-cognito-userpool-recoveryoption-name): String
  [Priority](#cfn-cognito-userpool-recoveryoption-priority): Integer
```

## Properties<a name="aws-properties-cognito-userpool-recoveryoption-properties"></a>

`Name`  <a name="cfn-cognito-userpool-recoveryoption-name"></a>
Specifies the recovery method for a user\.  
*Required*: No  
*Type*: String  
*Allowed values*: `admin_only | verified_email | verified_phone_number`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-cognito-userpool-recoveryoption-priority"></a>
A positive integer specifying priority of a method with 1 being the highest priority\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)