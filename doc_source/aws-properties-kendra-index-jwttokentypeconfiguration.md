# AWS::Kendra::Index JwtTokenTypeConfiguration<a name="aws-properties-kendra-index-jwttokentypeconfiguration"></a>

Configuration information for the JWT token type\.

## Syntax<a name="aws-properties-kendra-index-jwttokentypeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-jwttokentypeconfiguration-syntax.json"></a>

```
{
  "[ClaimRegex](#cfn-kendra-index-jwttokentypeconfiguration-claimregex)" : String,
  "[GroupAttributeField](#cfn-kendra-index-jwttokentypeconfiguration-groupattributefield)" : String,
  "[Issuer](#cfn-kendra-index-jwttokentypeconfiguration-issuer)" : String,
  "[KeyLocation](#cfn-kendra-index-jwttokentypeconfiguration-keylocation)" : String,
  "[SecretManagerArn](#cfn-kendra-index-jwttokentypeconfiguration-secretmanagerarn)" : String,
  "[URL](#cfn-kendra-index-jwttokentypeconfiguration-url)" : String,
  "[UserNameAttributeField](#cfn-kendra-index-jwttokentypeconfiguration-usernameattributefield)" : String
}
```

### YAML<a name="aws-properties-kendra-index-jwttokentypeconfiguration-syntax.yaml"></a>

```
  [ClaimRegex](#cfn-kendra-index-jwttokentypeconfiguration-claimregex): String
  [GroupAttributeField](#cfn-kendra-index-jwttokentypeconfiguration-groupattributefield): String
  [Issuer](#cfn-kendra-index-jwttokentypeconfiguration-issuer): String
  [KeyLocation](#cfn-kendra-index-jwttokentypeconfiguration-keylocation): String
  [SecretManagerArn](#cfn-kendra-index-jwttokentypeconfiguration-secretmanagerarn): String
  [URL](#cfn-kendra-index-jwttokentypeconfiguration-url): String
  [UserNameAttributeField](#cfn-kendra-index-jwttokentypeconfiguration-usernameattributefield): String
```

## Properties<a name="aws-properties-kendra-index-jwttokentypeconfiguration-properties"></a>

`ClaimRegex`  <a name="cfn-kendra-index-jwttokentypeconfiguration-claimregex"></a>
The regular expression that identifies the claim\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^\P{C}*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupAttributeField`  <a name="cfn-kendra-index-jwttokentypeconfiguration-groupattributefield"></a>
The group attribute field\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^\P{C}*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Issuer`  <a name="cfn-kendra-index-jwttokentypeconfiguration-issuer"></a>
The issuer of the token\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `65`  
*Pattern*: `^\P{C}*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyLocation`  <a name="cfn-kendra-index-jwttokentypeconfiguration-keylocation"></a>
The location of the key\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SECRET_MANAGER | URL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretManagerArn`  <a name="cfn-kendra-index-jwttokentypeconfiguration-secretmanagerarn"></a>
The Amazon Resource Name \(arn\) of the secret\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`URL`  <a name="cfn-kendra-index-jwttokentypeconfiguration-url"></a>
The signing key URL\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^(https?|ftp|file):\/\/([^\s]*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserNameAttributeField`  <a name="cfn-kendra-index-jwttokentypeconfiguration-usernameattributefield"></a>
The user name attribute field\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^\P{C}*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)