# AWS::ElastiCache::User Authentication<a name="aws-properties-elasticache-user-authentication"></a>

Indicates whether the user requires a password to authenticate\.

## Syntax<a name="aws-properties-elasticache-user-authentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-user-authentication-syntax.json"></a>

```
{
  "[PasswordCount](#cfn-elasticache-user-authentication-passwordcount)" : Integer,
  "[Type](#cfn-elasticache-user-authentication-type)" : String
}
```

### YAML<a name="aws-properties-elasticache-user-authentication-syntax.yaml"></a>

```
  [PasswordCount](#cfn-elasticache-user-authentication-passwordcount): Integer
  [Type](#cfn-elasticache-user-authentication-type): String
```

## Properties<a name="aws-properties-elasticache-user-authentication-properties"></a>

`PasswordCount`  <a name="cfn-elasticache-user-authentication-passwordcount"></a>
The number of passwords belonging to the user\. The maximum is two\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-elasticache-user-authentication-type"></a>
Indicates whether the user requires a password to authenticate\.  
*Required*: No  
*Type*: String  
*Allowed values*: `no-password | password`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)