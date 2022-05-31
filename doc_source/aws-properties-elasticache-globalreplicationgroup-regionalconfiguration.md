# AWS::ElastiCache::GlobalReplicationGroup RegionalConfiguration<a name="aws-properties-elasticache-globalreplicationgroup-regionalconfiguration"></a>

A list of the replication groups 

## Syntax<a name="aws-properties-elasticache-globalreplicationgroup-regionalconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-globalreplicationgroup-regionalconfiguration-syntax.json"></a>

```
{
  "[ReplicationGroupId](#cfn-elasticache-globalreplicationgroup-regionalconfiguration-replicationgroupid)" : String,
  "[ReplicationGroupRegion](#cfn-elasticache-globalreplicationgroup-regionalconfiguration-replicationgroupregion)" : String,
  "[ReshardingConfigurations](#cfn-elasticache-globalreplicationgroup-regionalconfiguration-reshardingconfigurations)" : [ ReshardingConfiguration, ... ]
}
```

### YAML<a name="aws-properties-elasticache-globalreplicationgroup-regionalconfiguration-syntax.yaml"></a>

```
  [ReplicationGroupId](#cfn-elasticache-globalreplicationgroup-regionalconfiguration-replicationgroupid): String
  [ReplicationGroupRegion](#cfn-elasticache-globalreplicationgroup-regionalconfiguration-replicationgroupregion): String
  [ReshardingConfigurations](#cfn-elasticache-globalreplicationgroup-regionalconfiguration-reshardingconfigurations): 
    - ReshardingConfiguration
```

## Properties<a name="aws-properties-elasticache-globalreplicationgroup-regionalconfiguration-properties"></a>

`ReplicationGroupId`  <a name="cfn-elasticache-globalreplicationgroup-regionalconfiguration-replicationgroupid"></a>
The name of the secondary cluster  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationGroupRegion`  <a name="cfn-elasticache-globalreplicationgroup-regionalconfiguration-replicationgroupregion"></a>
The Amazon region where the cluster is stored  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReshardingConfigurations`  <a name="cfn-elasticache-globalreplicationgroup-regionalconfiguration-reshardingconfigurations"></a>
A list of PreferredAvailabilityZones objects that specifies the configuration of a node group in the resharded cluster\.  
*Required*: No  
*Type*: List of [ReshardingConfiguration](aws-properties-elasticache-globalreplicationgroup-reshardingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)