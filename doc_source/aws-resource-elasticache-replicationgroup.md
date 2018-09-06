# AWS::ElastiCache::ReplicationGroup<a name="aws-resource-elasticache-replicationgroup"></a>

The `AWS::ElastiCache::ReplicationGroup` resource creates an Amazon ElastiCache Redis replication group\. A *replication group* is a collection of cache clusters, where one of the clusters is a primary read\-write cluster and the others are read\-only replicas\. 

**Topics**
+ [Syntax](#aws-resource-elasticache-replicationgroup-syntax)
+ [Properties](#aws-resource-elasticache-replicationgroup-properties)
+ [Return Values](#aws-resource-elasticache-replicationgroup-returnvalues)
+ [Examples](#aws-resource-elasticache-replicationgroup-examples)
+ [See Also](#aws-resource-elasticache-replicationgroup-seealso)

## Syntax<a name="aws-resource-elasticache-replicationgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticache-replicationgroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::ReplicationGroup",
  "Properties" : {
    "[AtRestEncryptionEnabled](#cfn-elasticache-replicationgroup-atrestencryptionenabled)" : Boolean,
    "[AuthToken](#cfn-elasticache-replicationgroup-authtoken)" : String,
    "[AutomaticFailoverEnabled](#cfn-elasticache-replicationgroup-automaticfailoverenabled)" : Boolean,
    "[AutoMinorVersionUpgrade](#cfn-elasticache-replicationgroup-autominorversionupgrade)" : Boolean,
    "[CacheNodeType](#cfn-elasticache-replicationgroup-cachenodetype)" : String,
    "[CacheParameterGroupName](#cfn-elasticache-replicationgroup-cacheparametergroupname)" : String,
    "[CacheSecurityGroupNames](#cfn-elasticache-replicationgroup-cachesecuritygroupnames)" : [ String, ... ],
    "[CacheSubnetGroupName](#cfn-elasticache-replicationgroup-cachesubnetgroupname)" : String,
    "[Engine](#cfn-elasticache-replicationgroup-engine)" : String,
    "[EngineVersion](#cfn-elasticache-replicationgroup-engineversion)" : String,
    "[NodeGroupConfiguration](#cfn-elasticache-replicationgroup-nodegroupconfiguration)" : [ [NodeGroupConfiguration](aws-properties-elasticache-replicationgroup-nodegroupconfiguration.md) ],
    "[NotificationTopicArn](#cfn-elasticache-replicationgroup-notificationtopicarn)" : String,
    "[NumCacheClusters](#cfn-elasticache-replicationgroup-numcacheclusters)" : Integer,
    "[NumNodeGroups](#cfn-elasticache-replicationgroup-numnodegroups)" : Integer,
    "[Port](#cfn-elasticache-replicationgroup-port)" : Integer,
    "[PreferredCacheClusterAZs](#cfn-elasticache-replicationgroup-preferredcacheclusterazs)" : [ String, ... ],
    "[PreferredMaintenanceWindow](#cfn-elasticache-replicationgroup-preferredmaintenancewindow)" : String,
    "[PrimaryClusterId](#cfn-elasticache-replicationgroup-primaryclusterid)" : String,
    "[ReplicasPerNodeGroup](#cfn-elasticache-replicationgroup-replicaspernodegroup)" : Integer,
    "[ReplicationGroupDescription](#cfn-elasticache-replicationgroup-replicationgroupdescription)" : String,
    "[ReplicationGroupId](#cfn-elasticache-replicationgroup-replicationgroupid)" : String,
    "[SecurityGroupIds](#cfn-elasticache-replicationgroup-securitygroupids)" : [ String, ... ],
    "[SnapshotArns](#cfn-elasticache-replicationgroup-snapshotarns)" : [ String, ... ],
    "[SnapshotName](#cfn-elasticache-replicationgroup-snapshotname)" : String,
    "[SnapshotRetentionLimit](#cfn-elasticache-replicationgroup-snapshotrentionlimit)" : Integer,
    "[SnapshottingClusterId](#cfn-elasticache-replicationgroup-snapshottingclusterid)" : String,
    "[SnapshotWindow](#cfn-elasticache-replicationgroup-snapshotwindow)" : String,
    "[Tags](#cfn-elasticache-replicationgroup-tags)" : Resource Tag, ...,
    "[TransitEncryptionEnabled](#cfn-elasticache-replicationgroup-transitencryptionenabled)" : Boolean
  }
}
```

### YAML<a name="aws-resource-elasticache-replicationgroup-syntax.yaml"></a>

```
Type: "AWS::ElastiCache::ReplicationGroup"
Properties: 
  [AtRestEncryptionEnabled](#cfn-elasticache-replicationgroup-atrestencryptionenabled): Boolean
  [AuthToken](#cfn-elasticache-replicationgroup-authtoken): String
  [AutomaticFailoverEnabled](#cfn-elasticache-replicationgroup-automaticfailoverenabled): Boolean
  [AutoMinorVersionUpgrade](#cfn-elasticache-replicationgroup-autominorversionupgrade): Boolean
  [CacheNodeType](#cfn-elasticache-replicationgroup-cachenodetype): String
  [CacheParameterGroupName](#cfn-elasticache-replicationgroup-cacheparametergroupname): String
  [CacheSecurityGroupNames](#cfn-elasticache-replicationgroup-cachesecuritygroupnames):
    - String
  [CacheSubnetGroupName](#cfn-elasticache-replicationgroup-cachesubnetgroupname): String
  [Engine](#cfn-elasticache-replicationgroup-engine): String
  [EngineVersion](#cfn-elasticache-replicationgroup-engineversion): String
  [NodeGroupConfiguration](#cfn-elasticache-replicationgroup-nodegroupconfiguration):
    - [NodeGroupConfiguration](aws-properties-elasticache-replicationgroup-nodegroupconfiguration.md)
  [NotificationTopicArn](#cfn-elasticache-replicationgroup-notificationtopicarn): String
  [NumCacheClusters](#cfn-elasticache-replicationgroup-numcacheclusters): Integer
  [NumNodeGroups](#cfn-elasticache-replicationgroup-numnodegroups): Integer
  [Port](#cfn-elasticache-replicationgroup-port): Integer
  [PreferredCacheClusterAZs](#cfn-elasticache-replicationgroup-preferredcacheclusterazs):
    - String
  [PreferredMaintenanceWindow](#cfn-elasticache-replicationgroup-preferredmaintenancewindow): String
  [PrimaryClusterId](#cfn-elasticache-replicationgroup-primaryclusterid): String
  [ReplicasPerNodeGroup](#cfn-elasticache-replicationgroup-replicaspernodegroup): Integer
  [ReplicationGroupDescription](#cfn-elasticache-replicationgroup-replicationgroupdescription): String
  [ReplicationGroupId](#cfn-elasticache-replicationgroup-replicationgroupid): String
  [SecurityGroupIds](#cfn-elasticache-replicationgroup-securitygroupids):
    - String
  [SnapshotArns](#cfn-elasticache-replicationgroup-snapshotarns):
    - String
  [SnapshotName](#cfn-elasticache-replicationgroup-snapshotname): String
  [SnapshotRetentionLimit](#cfn-elasticache-replicationgroup-snapshotrentionlimit): Integer
  [SnapshottingClusterId](#cfn-elasticache-replicationgroup-snapshottingclusterid): String
  [SnapshotWindow](#cfn-elasticache-replicationgroup-snapshotwindow): String
  [Tags](#cfn-elasticache-replicationgroup-tags)
    - Resource Tag
  [TransitEncryptionEnabled](#cfn-elasticache-replicationgroup-transitencryptionenabled): Boolean
```

## Properties<a name="aws-resource-elasticache-replicationgroup-properties"></a>

For more information about each property and valid values, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference*\.

`AtRestEncryptionEnabled`  <a name="cfn-elasticache-replicationgroup-atrestencryptionenabled"></a>
Indicates whether to enable encryption at rest\. The default value is `false`\. For more information about how you can use this property, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference*\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`AuthToken`  <a name="cfn-elasticache-replicationgroup-authtoken"></a>
The password that's used to access a password\-protected server\. For constraints, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference*\.  
`AuthToken` can be specified only on replication groups where `TransitEncryptionEnabled` is `true`\.  
For HIPAA compliance, you must specify `TransitEncryptionEnabled` as `true`, an `AuthToken`, and a `CacheSubnetGroupName`\.
*Required: *No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`AutomaticFailoverEnabled`  <a name="cfn-elasticache-replicationgroup-automaticfailoverenabled"></a>
Indicates whether Multi\-AZ is enabled\. When Multi\-AZ is enabled, a read\-only replica is automatically promoted to a read\-write primary cluster if the existing primary cluster fails\. If you specify `true`, you must specify a value greater than `1` for the `NumCacheClusters` property\. By default, AWS CloudFormation sets the value to `true`\.  
For Redis \(clustered mode enabled\) replication groups, you must enable automatic failover\.  
For information about Multi\-AZ constraints, see [Replication with Multi\-AZ and Automatic Failover \(Redis\)](http://docs.aws.amazon.com/AmazonElastiCache/latest/UserGuide/AutoFailover.html) in the *Amazon ElastiCache User Guide*\.  
You cannot enable automatic failover for Redis versions earlier than 2\.8\.6 or for T1 cache node types\. Automatic failover is supported on T2 node types only if you are running Redis version 3\.2\.4 or later with cluster mode enabled\.
If you specify the `PrimaryClusterId`, you can use only the following additional parameters:  
+ `AutomaticFailoverEnabled`
+ `NodeGroupConfiguration`
+ `NumCacheClusters`
+ `NumNodeGroups`
+ `PreferredCacheClusterAZs`
+ `ReplicationGroupDescription`
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-elasticache-replicationgroup-autominorversionupgrade"></a>
Currently, this property isn't used by ElastiCache\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CacheNodeType`  <a name="cfn-elasticache-replicationgroup-cachenodetype"></a>
The compute and memory capacity of nodes in the node group\. For valid values, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CacheParameterGroupName`  <a name="cfn-elasticache-replicationgroup-cacheparametergroupname"></a>
The name of the parameter group to associate with this replication group\. For valid and default values, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`CacheSecurityGroupNames`  <a name="cfn-elasticache-replicationgroup-cachesecuritygroupnames"></a>
A list of cache security group names to associate with this replication group\.  
If you specify the `CacheSecurityGroupNames` property, don't also specify the `SecurityGroupIds` property\.  
The `SecurityGroupIds` property is only for Amazon Virtual Private Cloud \(Amazon VPC\) security groups\. If you specify an Amazon VPC security group, the deployment fails\.
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CacheSubnetGroupName`  <a name="cfn-elasticache-replicationgroup-cachesubnetgroupname"></a>
The name of a cache subnet group to use for this replication group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Engine`  <a name="cfn-elasticache-replicationgroup-engine"></a>
The name of the cache engine to use for the cache clusters in this replication group\. Currently, you can specify only `redis`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EngineVersion`  <a name="cfn-elasticache-replicationgroup-engineversion"></a>
The version number of the cache engine to use for the cache clusters in this replication group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NodeGroupConfiguration`  <a name="cfn-elasticache-replicationgroup-nodegroupconfiguration"></a>
Configuration options for the node group \(shard\)\.  
If you specify the `PrimaryClusterId`, you can use only the following additional parameters:  
+ `AutomaticFailoverEnabled`
+ `NodeGroupConfiguration`
+ `NumCacheClusters`
+ `NumNodeGroups`
+ `PreferredCacheClusterAZs`
+ `ReplicationGroupDescription`
*Required*: No  
*Type*: List of [Amazon ElastiCache ReplicationGroup NodeGroupConfiguration](aws-properties-elasticache-replicationgroup-nodegroupconfiguration.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`NotificationTopicArn`  <a name="cfn-elasticache-replicationgroup-notificationtopicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service topic to which notifications are sent\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NumCacheClusters`  <a name="cfn-elasticache-replicationgroup-numcacheclusters"></a>
The number of cache clusters for this replication group\. If automatic failover is enabled, you must specify a value greater than `1`\. For valid values, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference Guide*\.  
If you specify more than one node group \(shard\), this property is ignored\. Use the `ReplicasPerNodeGroup` property instead\.  
If you specify the `PrimaryClusterId`, you can use only the following additional parameters:  
+ `AutomaticFailoverEnabled`
+ `NodeGroupConfiguration`
+ `NumCacheClusters`
+ `NumNodeGroups`
+ `PreferredCacheClusterAZs`
+ `ReplicationGroupDescription`
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NumNodeGroups`  <a name="cfn-elasticache-replicationgroup-numnodegroups"></a>
The number of node groups \(shards\) for this Redis \(clustered mode enabled\) replication group\. For Redis \(clustered mode disabled\), omit this property\.  
If you specify the `PrimaryClusterId`, you can use only the following additional parameters:  
+ `AutomaticFailoverEnabled`
+ `NodeGroupConfiguration`
+ `NumCacheClusters`
+ `NumNodeGroups`
+ `PreferredCacheClusterAZs`
+ `ReplicationGroupDescription`
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Port`  <a name="cfn-elasticache-replicationgroup-port"></a>
The port number on which each member of the replication group accepts connections\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PreferredCacheClusterAZs`  <a name="cfn-elasticache-replicationgroup-preferredcacheclusterazs"></a>
A list of Availability Zones in which the cache clusters in this replication group are created\.  
If you specify the `PrimaryClusterId`, you can use only the following additional parameters:  
+ `AutomaticFailoverEnabled`
+ `NodeGroupConfiguration`
+ `NumCacheClusters`
+ `NumNodeGroups`
+ `PreferredCacheClusterAZs`
+ `ReplicationGroupDescription`
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PreferredMaintenanceWindow`  <a name="cfn-elasticache-replicationgroup-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur\. Use the following format to specify a time range: `ddd:hh24:mi-ddd:hh24:mi` \(24H Clock UTC\)\. For example, you can specify `sun:22:00-sun:23:30` for Sunday from 10 PM to 11:30 PM\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`PrimaryClusterId`  <a name="cfn-elasticache-replicationgroup-primaryclusterid"></a>
The cache cluster that ElastiCache uses as the primary cluster for the replication group\. The cache cluster must have a status of `available`\.  
If you specify the `PrimaryClusterId`, you can use only the following additional parameters:  
+ `AutomaticFailoverEnabled`
+ `NodeGroupConfiguration`
+ `NumCacheClusters`
+ `NumNodeGroups`
+ `PreferredCacheClusterAZs`
+ `ReplicationGroupDescription`
*Required*: Conditional\. This property is optional if you specify the `NumCacheClusters`, `NumNodeGroups`, or `ReplicasPerNodeGroup` properties\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReplicasPerNodeGroup`  <a name="cfn-elasticache-replicationgroup-replicaspernodegroup"></a>
The number of replica nodes in each node group \(shard\)\. For valid values, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ReplicationGroupDescription`  <a name="cfn-elasticache-replicationgroup-replicationgroupdescription"></a>
A description of the replication group\.  
If you specify the `PrimaryClusterId`, you can use only the following additional parameters:  
+ `AutomaticFailoverEnabled`
+ `NodeGroupConfiguration`
+ `NumCacheClusters`
+ `NumNodeGroups`
+ `PreferredCacheClusterAZs`
+ `ReplicationGroupDescription`
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ReplicationGroupId`  <a name="cfn-elasticache-replicationgroup-replicationgroupid"></a>
An ID for the replication group\. If you don't specify an ID, AWS CloudFormation generates a unique physical ID\. For more information, see [Name Type](aws-properties-name.md)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SecurityGroupIds`  <a name="cfn-elasticache-replicationgroup-securitygroupids"></a>
A list of Amazon Virtual Private Cloud \(Amazon VPC\) security groups to associate with this replication group\.  
If you specify the `SecurityGroupIds` property, don't also specify the `CacheSecurityGroupNames` property\.  
The `CacheSecurityGroupNames` property is only for EC2\-Classic security groups\. If you specify an EC2\-Classic security group, the deployment fails\.
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SnapshotArns`  <a name="cfn-elasticache-replicationgroup-snapshotarns"></a>
A single\-element string list that specifies an ARN of a Redis `.rdb` snapshot file that is stored in Amazon Simple Storage Service \(Amazon S3\)\. The snapshot file populates the node group\. The Amazon S3 object name in the ARN cannot contain commas\. For example, you can specify `arn:aws:s3:::my_bucket/snapshot1.rdb`\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SnapshotName`  <a name="cfn-elasticache-replicationgroup-snapshotname"></a>
The name of a snapshot from which to restore data into the replication group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SnapshotRetentionLimit`  <a name="cfn-elasticache-replicationgroup-snapshotrentionlimit"></a>
The number of days that ElastiCache retains automatic snapshots before deleting them\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SnapshottingClusterId`  <a name="cfn-elasticache-replicationgroup-snapshottingclusterid"></a>
The ID of the cache cluster that ElastiCache uses as the daily snapshot source for the replication group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SnapshotWindow`  <a name="cfn-elasticache-replicationgroup-snapshotwindow"></a>
The time range \(in UTC\) when ElastiCache takes a daily snapshot of the node group that you specified in the `SnapshottingClusterId` property\. For example, you can specify `05:00-09:00`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-elasticache-replicationgroup-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this replication group\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TransitEncryptionEnabled`  <a name="cfn-elasticache-replicationgroup-transitencryptionenabled"></a>
Indicates whether to enable in\-transit encryption\. The default value is `false`\. For more information about how you can use this property, see [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference*\.  
If you enable `TransitEncryptionEnabled`, then you must also specify `CacheSubnetGroupName`\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-elasticache-replicationgroup-returnvalues"></a>

### Ref<a name="aws-resource-elasticache-replicationgroup-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

In the following example, the `Ref` function returns the name of the `myReplicationGroup` replication group, such as `abc12xmy3d1w3hv6`\.

```
{ "Ref": "myReplicationGroup" }
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-elasticache-replicationgroup-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`ConfigurationEndPoint.Address`  
The DNS hostname of the cache node\.

`ConfigurationEndPoint.Port`  
The port number that the cache engine is listening on\.

`PrimaryEndPoint.Address`  
The DNS address of the primary read\-write cache node\.

`PrimaryEndPoint.Port`  
The number of the port that the primary read\-write cache engine is listening on\.

`ReadEndPoint.Addresses`  
A string with a list of endpoints for the read\-only replicas\. The order of the addresses maps to the order of the ports from the `ReadEndPoint.Ports` attribute\.

`ReadEndPoint.Ports`  
A string with a list of ports for the read\-only replicas\. The order of the ports maps to the order of the addresses from the `ReadEndPoint.Addresses` attribute\.

`ReadEndPoint.Addresses.List`  
A list of endpoints for the read\-only replicas\. The order of the addresses maps to the order of the ports from the `ReadEndPoint.Ports.List` attribute\.

`ReadEndPoint.Ports.List`  
A list of ports for the read\-only replicas\. The order of the ports maps to the order of the addresses from the `ReadEndPoint.Addresses.List` attribute\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-elasticache-replicationgroup-examples"></a>

### Declare a Replication Group with Two Nodes<a name="aws-resource-elasticache-replicationgroup-example1"></a>

The following example declares a replication group with two nodes and automatic failover enabled\.

#### JSON<a name="aws-resource-elasticache-replicationgroup-example1.json"></a>

```
"myReplicationGroup" : {
  "Type": "AWS::ElastiCache::ReplicationGroup",
  "Properties": {
    "ReplicationGroupDescription" : "my description",
    "NumCacheClusters" : "2",
    "Engine" : "redis",
    "CacheNodeType" : "cache.m3.medium",
    "AutoMinorVersionUpgrade" : "true",
    "AutomaticFailoverEnabled" : "true",
    "CacheSubnetGroupName" : "subnetgroup",
    "EngineVersion" : "2.8.6",
    "PreferredMaintenanceWindow" : "wed:09:25-wed:22:30",
    "SnapshotRetentionLimit" : "4",
    "SnapshotWindow" : "03:30-05:30"
  }
}
```

#### YAML<a name="aws-resource-elasticache-replicationgroup-example1.yaml"></a>

```
myReplicationGroup: 
  Type: "AWS::ElastiCache::ReplicationGroup"
  Properties: 
    ReplicationGroupDescription: "my description"
    NumCacheClusters: "2"
    Engine: "redis"
    CacheNodeType: "cache.m3.medium"
    AutoMinorVersionUpgrade: "true"
    AutomaticFailoverEnabled: "true"
    CacheSubnetGroupName: "subnetgroup"
    EngineVersion: "2.8.6"
    PreferredMaintenanceWindow: "wed:09:25-wed:22:30"
    SnapshotRetentionLimit: "4"
    SnapshotWindow: "03:30-05:30"
```

### Declare a Replication Group with Two Node Groups<a name="aws-resource-elasticache-replicationgroup-example2"></a>

The following example declares a replication group with two nodes groups \(shards\) with three replicas in each group\.

#### JSON<a name="aws-resource-elasticache-replicationgroup-example2.json"></a>

```
"BasicReplicationGroup" : {
  "Type" : "AWS::ElastiCache::ReplicationGroup",
  "Properties" : {
    "AutomaticFailoverEnabled" : true,
    "AutoMinorVersionUpgrade" : true,
    "CacheNodeType" : "cache.r3.large",
    "CacheSubnetGroupName" : { "Ref" : "CacheSubnetGroup" },
    "Engine" : "redis",
    "EngineVersion" : "3.2",
    "NumNodeGroups" : "2",
    "ReplicasPerNodeGroup" : "3",
    "Port" : 6379,
    "PreferredMaintenanceWindow" : "sun:05:00-sun:09:00",
    "ReplicationGroupDescription" : "A sample replication group",
    "SecurityGroupIds" : [
      { "Ref" : "ReplicationGroupSG" }
    ],
    "SnapshotRetentionLimit" : 5,
    "SnapshotWindow" : "10:00-12:00"
  }
}
```

##### YAML<a name="aws-resource-elasticache-replicationgroup-example2.yaml"></a>

```
BasicReplicationGroup:
  Type: AWS::ElastiCache::ReplicationGroup
  Properties:
    AutomaticFailoverEnabled: true
    AutoMinorVersionUpgrade: true
    CacheNodeType: cache.r3.large
    CacheSubnetGroupName:
      Ref: CacheSubnetGroup
    Engine: redis
    EngineVersion: '3.2'
    NumNodeGroups: '2'
    ReplicasPerNodeGroup: '3'
    Port: 6379
    PreferredMaintenanceWindow: sun:05:00-sun:09:00
    ReplicationGroupDescription: A sample replication group
    SecurityGroupIds:
      - Ref: ReplicationGroupSG
    SnapshotRetentionLimit: 5
    SnapshotWindow: 10:00-12:00
```

## See Also<a name="aws-resource-elasticache-replicationgroup-seealso"></a>
+ [CreateReplicationGroup](http://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateReplicationGroup.html) in the *Amazon ElastiCache API Reference*