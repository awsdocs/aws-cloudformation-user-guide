# Amazon ElastiCache ReplicationGroup NodeGroupConfiguration<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration"></a>

`NodeGroupConfiguration` is a property of the [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md) resource that configures an Amazon ElastiCache \(ElastiCache\) Redis cluster node group\.

## Syntax<a name="w3ab2c21c14d962b5"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration-syntax.json"></a>

```
{
  "[PrimaryAvailabilityZone](#cfn-elasticache-replicationgroup-nodegroupconfiguration-primaryavailabilityzone)" : String,
  "[ReplicaAvailabilityZones](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicaavailabilityzones)" : [ String, ... ],
  "[ReplicaCount](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicacount)" : Integer,
  "[Slots](#cfn-elasticache-replicationgroup-nodegroupconfiguration-slots)" : String
}
```

### YAML<a name="aws-properties-elasticache-replicationgroup-nodegroupconfiguration-syntax.yaml"></a>

```
[PrimaryAvailabilityZone](#cfn-elasticache-replicationgroup-nodegroupconfiguration-primaryavailabilityzone): String
[ReplicaAvailabilityZones](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicaavailabilityzones):
  - String
[ReplicaCount](#cfn-elasticache-replicationgroup-nodegroupconfiguration-replicacount): Integer
[Slots](#cfn-elasticache-replicationgroup-nodegroupconfiguration-slots): String
```

## Properties<a name="w3ab2c21c14d962b7"></a>

`PrimaryAvailabilityZone`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-primaryavailabilityzone"></a>
The Availability Zone where ElastiCache launches the node group's primary node\.  
*Required*: No  
*Type*: String

`ReplicaAvailabilityZones`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-replicaavailabilityzones"></a>
A list of Availability Zones where ElastiCache launches the read replicas\. The number of Availability Zones must match the value of the `ReplicaCount` property or, if you don't specify the `ReplicaCount` property, the replication group's `ReplicasPerNodeGroup` property\.  
*Required*: No  
*Type*: List of String values

`ReplicaCount`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-replicacount"></a>
The number of read replica nodes in the node group\.  
*Required*: No  
*Type*: Integer

`Slots`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration-slots"></a>
A string of comma\-separated values where the first set of values are the slot numbers \(zero based\), and the second set of values are the keyspaces for each slot\. The following example specifies three slots \(numbered 0, 1, and 2\): `0,1,2,0-4999,5000-9999,10000-16,383`\.  
If you don't specify a value, ElastiCache allocates keys equally among each slot\.  
*Required*: No  
*Type*: String