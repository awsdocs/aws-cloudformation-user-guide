# AWS::ElastiCache::User AuthenticationMode<a name="aws-properties-elasticache-user-authenticationmode"></a>

Specifies the authentication mode to use\.

## Syntax<a name="aws-properties-elasticache-user-authenticationmode-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-user-authenticationmode-syntax.json"></a>

```
{
  "[Passwords](#cfn-elasticache-user-authenticationmode-passwords)" : [ String, ... ],
  "[Type](#cfn-elasticache-user-authenticationmode-type)" : String
}
```

### YAML<a name="aws-properties-elasticache-user-authenticationmode-syntax.yaml"></a>

```
  [Passwords](#cfn-elasticache-user-authenticationmode-passwords): 
    - String
  [Type](#cfn-elasticache-user-authenticationmode-type): String
```

## Properties<a name="aws-properties-elasticache-user-authenticationmode-properties"></a>

`Passwords`  <a name="cfn-elasticache-user-authenticationmode-passwords"></a>
Specifies the passwords to use for authentication if `Type` is set to `password`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-elasticache-user-authenticationmode-type"></a>
Specifies the authentication type\. Possible options are IAM authentication, password and no password\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `iam | no-password-required | password`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)