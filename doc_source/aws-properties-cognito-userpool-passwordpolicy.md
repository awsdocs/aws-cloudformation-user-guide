# AWS::Cognito::UserPool PasswordPolicy<a name="aws-properties-cognito-userpool-passwordpolicy"></a>

`PasswordPolicy` is a subproperty of the [Policies](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-userpool-policies.html) property that defines the password policy of an Amazon Cognito User Pool\.

## Syntax<a name="aws-properties-cognito-userpool-passwordpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpool-passwordpolicy-syntax.json"></a>

```
{
  "[MinimumLength](#cfn-cognito-userpool-passwordpolicy-minimumlength)" : Integer,
  "[RequireLowercase](#cfn-cognito-userpool-passwordpolicy-requirelowercase)" : Boolean,
  "[RequireNumbers](#cfn-cognito-userpool-passwordpolicy-requirenumbers)" : Boolean,
  "[RequireSymbols](#cfn-cognito-userpool-passwordpolicy-requiresymbols)" : Boolean,
  "[RequireUppercase](#cfn-cognito-userpool-passwordpolicy-requireuppercase)" : Boolean,
  "[TemporaryPasswordValidityDays](#cfn-cognito-userpool-passwordpolicy-temporarypasswordvaliditydays)" : Double
}
```

### YAML<a name="aws-properties-cognito-userpool-passwordpolicy-syntax.yaml"></a>

```
  [MinimumLength](#cfn-cognito-userpool-passwordpolicy-minimumlength): Integer
  [RequireLowercase](#cfn-cognito-userpool-passwordpolicy-requirelowercase): Boolean
  [RequireNumbers](#cfn-cognito-userpool-passwordpolicy-requirenumbers): Boolean
  [RequireSymbols](#cfn-cognito-userpool-passwordpolicy-requiresymbols): Boolean
  [RequireUppercase](#cfn-cognito-userpool-passwordpolicy-requireuppercase): Boolean
  [TemporaryPasswordValidityDays](#cfn-cognito-userpool-passwordpolicy-temporarypasswordvaliditydays): Double
```

## Properties<a name="aws-properties-cognito-userpool-passwordpolicy-properties"></a>

`MinimumLength`  <a name="cfn-cognito-userpool-passwordpolicy-minimumlength"></a>
The minimum length of the password policy that you have set\. Cannot be less than 6\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `6`  
*Maximum*: `99`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireLowercase`  <a name="cfn-cognito-userpool-passwordpolicy-requirelowercase"></a>
In the password policy that you have set, refers to whether you have required users to use at least one lowercase letter in their password\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireNumbers`  <a name="cfn-cognito-userpool-passwordpolicy-requirenumbers"></a>
In the password policy that you have set, refers to whether you have required users to use at least one number in their password\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireSymbols`  <a name="cfn-cognito-userpool-passwordpolicy-requiresymbols"></a>
In the password policy that you have set, refers to whether you have required users to use at least one symbol in their password\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireUppercase`  <a name="cfn-cognito-userpool-passwordpolicy-requireuppercase"></a>
In the password policy that you have set, refers to whether you have required users to use at least one uppercase letter in their password\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemporaryPasswordValidityDays`  <a name="cfn-cognito-userpool-passwordpolicy-temporarypasswordvaliditydays"></a>
In the password policy you have set, refers to the number of days a temporary password is valid\. If the user does not sign\-in during this time, their password will need to be reset by an administrator\.  
When you set `TemporaryPasswordValidityDays` for a user pool, you will no longer be able to set the deprecated `UnusedAccountValidityDays` value for that user pool\.
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `365`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
