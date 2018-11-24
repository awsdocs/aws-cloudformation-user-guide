# Amazon ElastiCache ReplicationGroup NodeGroupConfiguration<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration"></a>

`NodeGroupConfiguration` is a property of the [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md) resource that configures an Amazon ElastiCache \(ElastiCache\) Redis cluster node group\.

## Syntax<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration.syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration-syntax.json"></a>

```
{
  "[NodeGroupId](#cfn-elasticache-replicationgroup-nodegroupconfiguration-nodegroupid)" : String,
  "[PrimaryAvailabilityZone](#cfn-elasticache-replicationgroup-nodegroupconfiguration-primaryavailabilityzone)" : String,
  "[ReplicaAvailabilityZones](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicaavailabilityzones)" : [ String, ... ],
  "[ReplicaCount](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicacount)" : Integer,
  "[Slots](#cfn-elasticache-replicationgroup-nodegroupconfiguration-slots)" : String
}
```

### YAML<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration-syntax.yaml"></a>

```
[NodeGroupId](#cfn-elasticache-replicationgroup-nodegroupconfiguration-nodegroupid): String
[PrimaryAvailabilityZone](#cfn-elasticache-replicationgroup-nodegroupconfiguration-primaryavailabilityzone): String
[ReplicaAvailabilityZones](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicaavailabilityzones):
  - String
[ReplicaCount](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicacount): Integer
[Slots](#cfn-elasticache-replicationgroup-nodegroupconfiguration-slots): String
```

## Properties<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration-properties"></a>

`NodeGroupId`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-nodegroupid"></a>
Either the ElastiCache for Redis supplied 4\-digit id or a user supplied id for the node group these configuration values apply to\.  
Length Constraints: Minimum length of 1\. Maximum length of 4\.  
Pattern: `\d+`  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. Update requires no interruption if the resource contains an `UseOnlineResharding` update policy set to `true`\. Update requires replacement if the resource does not contain an `UseOnlineResharding` update policy, or the policy is set to `false`\. For more information, see [UseOnlineResharding Policy](aws-attribute-updatepolicy.md#cfn-attributes-updatepolicy-useonlineresharding)\.

`PrimaryAvailabilityZone`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-primaryavailabilityzone"></a>
The Availability Zone where ElastiCache launches the node group's primary node\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ReplicaAvailabilityZones`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-replicaavailabilityzones"></a>
A list of Availability Zones where ElastiCache launches the read replicas\. The number of Availability Zones must match the value of the `ReplicaCount` property or, if you don't specify the `ReplicaCount` property, the replication group's `ReplicasPerNodeGroup` property\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ReplicaCount`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-replicacount"></a>
The number of read replica nodes in the node group\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Slots`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-slots"></a>
A string of comma\-separated values where the first set of values are the slot numbers \(zero based\), and the second set of values are the keyspaces for each slot\. The following example specifies three slots \(numbered 0, 1, and 2\): `0,1,2,0-4999,5000-9999,10000-16,383`\.  
If you don't specify a value, ElastiCache allocates keys equally among each slot\.  
When you use an `UseOnlineResharding` update policy to update the number of node groups without interruption, ElastiCache evenly distributes the keyspaces between the specified number of slots\. This cannot be updated later\. Therefore, after updating the number of node groups in this way, you should remove the value specified for the `Slots` property of each `NodeGroupConfiguration` from the stack template, as it no longer reflects the actual values in each node group\. For more information, see [UseOnlineResharding Policy](aws-attribute-updatepolicy.md#cfn-attributes-updatepolicy-useonlineresharding)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)