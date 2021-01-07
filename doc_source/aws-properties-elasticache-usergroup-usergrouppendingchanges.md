# AWS::ElastiCache::UserGroup UserGroupPendingChanges<a name="aws-properties-elasticache-usergroup-usergrouppendingchanges"></a>

Returns the updates being applied to the user group\.

## Syntax<a name="aws-properties-elasticache-usergroup-usergrouppendingchanges-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-usergroup-usergrouppendingchanges-syntax.json"></a>

```
{
  "[UserIdsToAdd](#cfn-elasticache-usergroup-usergrouppendingchanges-useridstoadd)" : [ String, ... ],
  "[UserIdsToRemove](#cfn-elasticache-usergroup-usergrouppendingchanges-useridstoremove)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticache-usergroup-usergrouppendingchanges-syntax.yaml"></a>

```
  [UserIdsToAdd](#cfn-elasticache-usergroup-usergrouppendingchanges-useridstoadd): 
    - String
  [UserIdsToRemove](#cfn-elasticache-usergroup-usergrouppendingchanges-useridstoremove): 
    - String
```

## Properties<a name="aws-properties-elasticache-usergroup-usergrouppendingchanges-properties"></a>

`UserIdsToAdd`  <a name="cfn-elasticache-usergroup-usergrouppendingchanges-useridstoadd"></a>
The list of user IDs to add\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserIdsToRemove`  <a name="cfn-elasticache-usergroup-usergrouppendingchanges-useridstoremove"></a>
The list of user IDs to remove\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)