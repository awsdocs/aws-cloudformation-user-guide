# AWS::Cognito::UserPool Policies<a name="aws-properties-cognito-userpool-policies"></a>

The policy associated with a user pool\.

## Syntax<a name="aws-properties-cognito-userpool-policies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-policies-syntax.json"></a>

```
{
  "[PasswordPolicy](#cfn-cognito-userpool-policies-passwordpolicy)" : PasswordPolicy
}
```

### YAML<a name="aws-properties-cognito-userpool-policies-syntax.yaml"></a>

```
  [PasswordPolicy](#cfn-cognito-userpool-policies-passwordpolicy): 
    PasswordPolicy
```

## Properties<a name="aws-properties-cognito-userpool-policies-properties"></a>

`PasswordPolicy`  <a name="cfn-cognito-userpool-policies-passwordpolicy"></a>
The password policy\.  
*Required*: No  
*Type*: [PasswordPolicy](aws-properties-cognito-userpool-passwordpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)