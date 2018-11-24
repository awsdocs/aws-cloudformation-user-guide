# Amazon Cognito UserPool Policies<a name="aws-properties-cognito-userpool-policies"></a>

`Policies` is a property of the [AWS::Cognito::UserPool](aws-resource-cognito-userpool.md) resource that defines the password policies of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-policies-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-policies-syntax.json"></a>

```
{
  "[PasswordPolicy](#cfn-cognito-userpool-policies-passwordpolicy)" : PasswordPolicy
}
```

### YAML<a name="aws-properties-cognito-userpool-policies-syntax.yaml"></a>

```
[PasswordPolicy](#cfn-cognito-userpool-policies-passwordpolicy): PasswordPolicy
```

## Properties<a name="aws-properties-cognito-userpool-policies-properties"></a>

`PasswordPolicy`  <a name="cfn-cognito-userpool-policies-passwordpolicy"></a>
Specifies information about the user pool password policy\.  
*Type*: [Amazon Cognito UserPool PasswordPolicy](aws-properties-cognito-userpool-passwordpolicy.md)  
*Required*: No