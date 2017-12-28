# Amazon Cognito UserPool PasswordPolicy<a name="aws-properties-cognito-userpool-passwordpolicy"></a>

`PasswordPolicy` is a subproperty of the [Amazon Cognito UserPool Policies](aws-properties-cognito-userpool-policies.md) property that defines the password policy of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-passwordpolicy-syntax"></a>

### JSON<a name="aws-properties-cognito-userpool-passwordpolicy-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-minimumlength)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requirelowercase)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requirenumbers)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requiresymbols)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requireuppercase)" : Boolean
}
```

### YAML<a name="aws-properties-cognito-userpool-passwordpolicy-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-minimumlength): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requirelowercase): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requirenumbers): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requiresymbols): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cognito-userpool-passwordpolicy-requireuppercase): Boolean
```

## Properties<a name="aws-properties-cognito-userpool-passwordpolicy-properties"></a>

`MinimumLength`  
The minimum length of the password policy that you have set\. Cannot be less than 6\.  
*Type*: Integer  
*Required: *No

`RequireLowercase`  
In the password policy that you have set, refers to whether you have required users to use at least one lowercase letter in their password\.  
*Type*: Boolean  
*Required: *No

`RequireNumbers`  
In the password policy that you have set, refers to whether you have required users to use at least one number in their password\.  
*Type*: Boolean  
*Required: *No

`RequireSymbols`  
In the password policy that you have set, refers to whether you have required users to use at least one symbol in their password\.  
*Type*: Boolean  
*Required: *No

`RequireUppercase`  
In the password policy that you have set, refers to whether you have required users to use at least one uppercase letter in their password\.  
*Type*: Boolean  
*Required: *No