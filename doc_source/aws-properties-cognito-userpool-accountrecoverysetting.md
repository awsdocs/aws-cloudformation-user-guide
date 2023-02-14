# AWS::Cognito::UserPool AccountRecoverySetting<a name="aws-properties-cognito-userpool-accountrecoverysetting"></a>

Use this setting to define which verified available method a user can use to recover their password when they call `ForgotPassword`\. It allows you to define a preferred method when a user has more than one method available\. With this setting, SMS does not qualify for a valid password recovery mechanism if the user also has SMS MFA enabled\. In the absence of this setting, Cognito uses the legacy behavior to determine the recovery method where SMS is preferred over email\.

## Syntax<a name="aws-properties-cognito-userpool-accountrecoverysetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-accountrecoverysetting-syntax.json"></a>

```
{
  "[RecoveryMechanisms](#cfn-cognito-userpool-accountrecoverysetting-recoverymechanisms)" : [ RecoveryOption, ... ]
}
```

### YAML<a name="aws-properties-cognito-userpool-accountrecoverysetting-syntax.yaml"></a>

```
  [RecoveryMechanisms](#cfn-cognito-userpool-accountrecoverysetting-recoverymechanisms): 
    - RecoveryOption
```

## Properties<a name="aws-properties-cognito-userpool-accountrecoverysetting-properties"></a>

`RecoveryMechanisms`  <a name="cfn-cognito-userpool-accountrecoverysetting-recoverymechanisms"></a>
The list of `RecoveryOptionTypes`\.  
*Required*: No  
*Type*: List of [RecoveryOption](aws-properties-cognito-userpool-recoveryoption.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)