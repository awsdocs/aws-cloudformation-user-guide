# AWS::ElastiCache::UserGroup<a name="aws-resource-elasticache-usergroup"></a>

For Redis engine version 6\.0 onwards: Creates a Redis user group\. For more information, see [Using Role Based Access Control \(RBAC\)](https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/Clusters.RBAC.html) 

## Syntax<a name="aws-resource-elasticache-usergroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-usergroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::UserGroup",
  "Properties" : {
      "[Engine](#cfn-elasticache-usergroup-engine)" : String,
      "[Tags](#cfn-elasticache-usergroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserGroupId](#cfn-elasticache-usergroup-usergroupid)" : String,
      "[UserIds](#cfn-elasticache-usergroup-userids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-elasticache-usergroup-syntax.yaml"></a>

```
Type: AWS::ElastiCache::UserGroup
Properties: 
  [Engine](#cfn-elasticache-usergroup-engine): String
  [Tags](#cfn-elasticache-usergroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserGroupId](#cfn-elasticache-usergroup-usergroupid): String
  [UserIds](#cfn-elasticache-usergroup-userids): 
    - String
```

## Properties<a name="aws-resource-elasticache-usergroup-properties"></a>

`Engine`  <a name="cfn-elasticache-usergroup-engine"></a>
The current supported value is redis\.   
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-zA-Z]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-elasticache-usergroup-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserGroupId`  <a name="cfn-elasticache-usergroup-usergroupid"></a>
The ID of the user group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserIds`  <a name="cfn-elasticache-usergroup-userids"></a>
The list of user IDs that belong to the user group\. A user named `default` must be included\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-elasticache-usergroup-return-values"></a>

### Ref<a name="aws-resource-elasticache-usergroup-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-elasticache-usergroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-elasticache-usergroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the user group\.

`Status`  <a name="Status-fn::getatt"></a>
Indicates user group status\. Can be "creating", "active", "modifying", "deleting"\.