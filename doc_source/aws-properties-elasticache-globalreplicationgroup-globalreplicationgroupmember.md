# AWS::ElastiCache::GlobalReplicationGroup GlobalReplicationGroupMember<a name="aws-properties-elasticache-globalreplicationgroup-globalreplicationgroupmember"></a>

A member of a Global Datastore\. It contains the Replication Group Id, the AWS region and the role of the replication group\. 

## Syntax<a name="aws-properties-elasticache-globalreplicationgroup-globalreplicationgroupmember-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-globalreplicationgroup-globalreplicationgroupmember-syntax.json"></a>

```
{
  "[ReplicationGroupId](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-replicationgroupid)" : String,
  "[ReplicationGroupRegion](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-replicationgroupregion)" : String,
  "[Role](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-role)" : String,
  "[Status](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-status)" : String
}
```

### YAML<a name="aws-properties-elasticache-globalreplicationgroup-globalreplicationgroupmember-syntax.yaml"></a>

```
  [ReplicationGroupId](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-replicationgroupid): String
  [ReplicationGroupRegion](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-replicationgroupregion): String
  [Role](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-role): String
  [Status](#cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-status): String
```

## Properties<a name="aws-properties-elasticache-globalreplicationgroup-globalreplicationgroupmember-properties"></a>

`ReplicationGroupId`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-replicationgroupid"></a>
The replication group id of the Global Datastore member\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationGroupRegion`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-replicationgroupregion"></a>
The AWS region of the Global Datastore member\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-role"></a>
Indicates the role of the replication group, primary or secondary\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-elasticache-globalreplicationgroup-globalreplicationgroupmember-status"></a>
The status of the membership of the replication group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)