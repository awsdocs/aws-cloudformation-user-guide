# AWS::ElastiCache::User<a name="aws-resource-elasticache-user"></a>

For Redis engine version 6\.x onwards: Creates a Redis user\. [Using Role Based Access Control \(RBAC\)](https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/Clusters.RBAC.html)\.

## Syntax<a name="aws-resource-elasticache-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-user-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::User",
  "Properties" : {
      "[AccessString](#cfn-elasticache-user-accessstring)" : String,
      "[Engine](#cfn-elasticache-user-engine)" : String,
      "[NoPasswordRequired](#cfn-elasticache-user-nopasswordrequired)" : Boolean,
      "[Passwords](#cfn-elasticache-user-passwords)" : PasswordList,
      "[UserId](#cfn-elasticache-user-userid)" : String,
      "[UserName](#cfn-elasticache-user-username)" : String
    }
}
```

### YAML<a name="aws-resource-elasticache-user-syntax.yaml"></a>

```
Type: AWS::ElastiCache::User
Properties: 
  [AccessString](#cfn-elasticache-user-accessstring): 
    String
  [Engine](#cfn-elasticache-user-engine): String
  [NoPasswordRequired](#cfn-elasticache-user-nopasswordrequired): Boolean
  [Passwords](#cfn-elasticache-user-passwords): 
    PasswordList
  [UserId](#cfn-elasticache-user-userid): String
  [UserName](#cfn-elasticache-user-username): String
```

## Properties<a name="aws-resource-elasticache-user-properties"></a>

`AccessString`  <a name="cfn-elasticache-user-accessstring"></a>
Access permissions string used for this user\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-elasticache-user-engine"></a>
The current supported value is Redis\.   
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-zA-Z]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NoPasswordRequired`  <a name="cfn-elasticache-user-nopasswordrequired"></a>
Indicates a password is not required for this user\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Passwords`  <a name="cfn-elasticache-user-passwords"></a>
Passwords used for this user\. You can create up to two passwords for each user\.  
*Required*: No  
*Type*: [PasswordList](aws-properties-elasticache-user-passwordlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserId`  <a name="cfn-elasticache-user-userid"></a>
The ID of the user\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Pattern*: `[a-zA-Z][a-zA-Z0-9\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserName`  <a name="cfn-elasticache-user-username"></a>
The username of the user\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-elasticache-user-return-values"></a>

### Ref<a name="aws-resource-elasticache-user-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-elasticache-user-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-elasticache-user-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the user\.

`Authentication`  <a name="Authentication-fn::getatt"></a>
Denotes whether the user requires a password to authenticate\.

`Status`  <a name="Status-fn::getatt"></a>
Indicates the user status\. Can be "active", "modifying" or "deleting"\.

`UserGroupIds`  <a name="UserGroupIds-fn::getatt"></a>
Returns a list of the user group IDs the user belongs to\.