# Amazon Cognito UserPool PasswordPolicy<a name="aws-properties-cognito-userpool-passwordpolicy"></a>

`PasswordPolicy` is a subproperty of the [Amazon Cognito UserPool Policies](aws-properties-cognito-userpool-policies.md) property that defines the password policy of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-passwordpolicy-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-passwordpolicy-syntax.json"></a>

```
{
  "[MinimumLength](#cfn-cognito-userpool-passwordpolicy-minimumlength)" : Integer,
  "[RequireLowercase](#cfn-cognito-userpool-passwordpolicy-requirelowercase)" : Boolean,
  "[RequireNumbers](#cfn-cognito-userpool-passwordpolicy-requirenumbers)" : Boolean,
  "[RequireSymbols](#cfn-cognito-userpool-passwordpolicy-requiresymbols)" : Boolean,
  "[RequireUppercase](#cfn-cognito-userpool-passwordpolicy-requireuppercase)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpool-passwordpolicy-syntax.yaml"></a>

```
[MinimumLength](#cfn-cognito-userpool-passwordpolicy-minimumlength): Integer
[RequireLowercase](#cfn-cognito-userpool-passwordpolicy-requirelowercase): Boolean
[RequireNumbers](#cfn-cognito-userpool-passwordpolicy-requirenumbers): Boolean
[RequireSymbols](#cfn-cognito-userpool-passwordpolicy-requiresymbols): Boolean
[RequireUppercase](#cfn-cognito-userpool-passwordpolicy-requireuppercase): Boolean
```

## Properties<a name="aws-properties-cognito-userpool-passwordpolicy-properties"></a>

`MinimumLength`  <a name="cfn-cognito-userpool-passwordpolicy-minimumlength"></a>
The minimum length of the password policy that you have set\. Cannot be less than 6\.  
*Type*: Integer  
*Required*: No

`RequireLowercase`  <a name="cfn-cognito-userpool-passwordpolicy-requirelowercase"></a>
In the password policy that you have set, refers to whether you have required users to use at least one lowercase letter in their password\.  
*Type*: Boolean  
*Required*: No

`RequireNumbers`  <a name="cfn-cognito-userpool-passwordpolicy-requirenumbers"></a>
In the password policy that you have set, refers to whether you have required users to use at least one number in their password\.  
*Type*: Boolean  
*Required*: No

`RequireSymbols`  <a name="cfn-cognito-userpool-passwordpolicy-requiresymbols"></a>
In the password policy that you have set, refers to whether you have required users to use at least one symbol in their password\.  
*Type*: Boolean  
*Required*: No

`RequireUppercase`  <a name="cfn-cognito-userpool-passwordpolicy-requireuppercase"></a>
In the password policy that you have set, refers to whether you have required users to use at least one uppercase letter in their password\.  
*Type*: Boolean  
*Required*: No