# AWS::ElastiCache::UserGroup ReplicationGroupIdList<a name="aws-properties-elasticache-usergroup-replicationgroupidlist"></a>

A list of replication groups\. Each item in the list contains detailed information about one replication group\.

## Syntax<a name="aws-properties-elasticache-usergroup-replicationgroupidlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-usergroup-replicationgroupidlist-syntax.json"></a>

```
{
  "[ReplicationGroupIdList](#cfn-elasticache-usergroup-replicationgroupidlist-replicationgroupidlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-elasticache-usergroup-replicationgroupidlist-syntax.yaml"></a>

```
  [ReplicationGroupIdList](#cfn-elasticache-usergroup-replicationgroupidlist-replicationgroupidlist): 
    - String
```

## Properties<a name="aws-properties-elasticache-usergroup-replicationgroupidlist-properties"></a>

`ReplicationGroupIdList`  <a name="cfn-elasticache-usergroup-replicationgroupidlist-replicationgroupidlist"></a>
A list of replication groups\. Each item in the list contains detailed information about one replication group\.  
*Required*: No  
*Type*: [List](#aws-properties-elasticache-usergroup-replicationgroupidlist) of [String](#aws-properties-elasticache-usergroup-replicationgroupidlist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)