# AWS::ElastiCache::User PasswordList<a name="aws-properties-elasticache-user-passwordlist"></a>

Passwords used for this user\. You can create up to two passwords for each user\.

## Syntax<a name="aws-properties-elasticache-user-passwordlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-user-passwordlist-syntax.json"></a>

```
{
  "[PasswordList](#cfn-elasticache-user-passwordlist-passwordlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticache-user-passwordlist-syntax.yaml"></a>

```
  [PasswordList](#cfn-elasticache-user-passwordlist-passwordlist): 
    - String
```

## Properties<a name="aws-properties-elasticache-user-passwordlist-properties"></a>

`PasswordList`  <a name="cfn-elasticache-user-passwordlist-passwordlist"></a>
Passwords used for this user\. You can create up to two passwords for each user\.  
*Required*: No  
*Type*: [List](#aws-properties-elasticache-user-passwordlist) of [String](#aws-properties-elasticache-user-passwordlist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)