# AWS::ElastiCache::CacheCluster<a name="aws-properties-elasticache-cache-cluster"></a>

The AWS::ElastiCache::CacheCluster type creates an Amazon ElastiCache cache cluster\. 

## Syntax<a name="aws-properties-elasticache-cache-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-cache-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::CacheCluster",
  "Properties" : {
      "[AutoMinorVersionUpgrade](#cfn-elasticache-cachecluster-autominorversionupgrade)" : Boolean,
      "[AZMode](#cfn-elasticache-cachecluster-azmode)" : String,
      "[CacheNodeType](#cfn-elasticache-cachecluster-cachenodetype)" : String,
      "[CacheParameterGroupName](#cfn-elasticache-cachecluster-cacheparametergroupname)" : String,
      "[CacheSecurityGroupNames](#cfn-elasticache-cachecluster-cachesecuritygroupnames)" : [ String, ... ],
      "[CacheSubnetGroupName](#cfn-elasticache-cachecluster-cachesubnetgroupname)" : String,
      "[ClusterName](#cfn-elasticache-cachecluster-clustername)" : String,
      "[Engine](#cfn-elasticache-cachecluster-engine)" : String,
      "[EngineVersion](#cfn-elasticache-cachecluster-engineversion)" : String,
      "[NotificationTopicArn](#cfn-elasticache-cachecluster-notificationtopicarn)" : String,
      "[NumCacheNodes](#cfn-elasticache-cachecluster-numcachenodes)" : Integer,
      "[Port](#cfn-elasticache-cachecluster-port)" : Integer,
      "[PreferredAvailabilityZone](#cfn-elasticache-cachecluster-preferredavailabilityzone)" : String,
      "[PreferredAvailabilityZones](#cfn-elasticache-cachecluster-preferredavailabilityzones)" : [ String, ... ],
      "[PreferredMaintenanceWindow](#cfn-elasticache-cachecluster-preferredmaintenancewindow)" : String,
      "[SnapshotArns](#cfn-elasticache-cachecluster-snapshotarns)" : [ String, ... ],
      "[SnapshotName](#cfn-elasticache-cachecluster-snapshotname)" : String,
      "[SnapshotRetentionLimit](#cfn-elasticache-cachecluster-snapshotretentionlimit)" : Integer,
      "[SnapshotWindow](#cfn-elasticache-cachecluster-snapshotwindow)" : String,
      "[Tags](#cfn-elasticache-cachecluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcSecurityGroupIds](#cfn-elasticache-cachecluster-vpcsecuritygroupids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-properties-elasticache-cache-cluster-syntax.yaml"></a>

```
Type: AWS::ElastiCache::CacheCluster
Properties: 
  [AutoMinorVersionUpgrade](#cfn-elasticache-cachecluster-autominorversionupgrade): Boolean
  [AZMode](#cfn-elasticache-cachecluster-azmode): String
  [CacheNodeType](#cfn-elasticache-cachecluster-cachenodetype): String
  [CacheParameterGroupName](#cfn-elasticache-cachecluster-cacheparametergroupname): String
  [CacheSecurityGroupNames](#cfn-elasticache-cachecluster-cachesecuritygroupnames): 
    - String
  [CacheSubnetGroupName](#cfn-elasticache-cachecluster-cachesubnetgroupname): String
  [ClusterName](#cfn-elasticache-cachecluster-clustername): String
  [Engine](#cfn-elasticache-cachecluster-engine): String
  [EngineVersion](#cfn-elasticache-cachecluster-engineversion): String
  [NotificationTopicArn](#cfn-elasticache-cachecluster-notificationtopicarn): String
  [NumCacheNodes](#cfn-elasticache-cachecluster-numcachenodes): Integer
  [Port](#cfn-elasticache-cachecluster-port): Integer
  [PreferredAvailabilityZone](#cfn-elasticache-cachecluster-preferredavailabilityzone): String
  [PreferredAvailabilityZones](#cfn-elasticache-cachecluster-preferredavailabilityzones): 
    - String
  [PreferredMaintenanceWindow](#cfn-elasticache-cachecluster-preferredmaintenancewindow): String
  [SnapshotArns](#cfn-elasticache-cachecluster-snapshotarns): 
    - String
  [SnapshotName](#cfn-elasticache-cachecluster-snapshotname): String
  [SnapshotRetentionLimit](#cfn-elasticache-cachecluster-snapshotretentionlimit): Integer
  [SnapshotWindow](#cfn-elasticache-cachecluster-snapshotwindow): String
  [Tags](#cfn-elasticache-cachecluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcSecurityGroupIds](#cfn-elasticache-cachecluster-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-properties-elasticache-cache-cluster-properties"></a>

`AutoMinorVersionUpgrade`  <a name="cfn-elasticache-cachecluster-autominorversionupgrade"></a>
This parameter is currently disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AZMode`  <a name="cfn-elasticache-cachecluster-azmode"></a>
Specifies whether the nodes in this Memcached cluster are created in a single Availability Zone or created across multiple Availability Zones in the cluster's region\.  
This parameter is only supported for Memcached clusters\.  
If the `AZMode` and `PreferredAvailabilityZones` are not specified, ElastiCache assumes `single-az` mode\.  
*Required*: No  
*Type*: String  
*Allowed values*: `cross-az | single-az`  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`CacheNodeType`  <a name="cfn-elasticache-cachecluster-cachenodetype"></a>
The compute and memory capacity of the nodes in the node group \(shard\)\.  
The following node types are supported by ElastiCache\. Generally speaking, the current generation types provide more memory and computational power at lower cost when compared to their equivalent previous generation counterparts\. Changing the CacheNodeType of a Memcached instance is currently not supported\. If you need to scale using Memcached, we recommend forcing a replacement update by changing the `LogicalResourceId` of the resource\.  
+ General purpose:
  + Current generation: 

    **M6g node types:** `cache.m6g.large`, `cache.m6g.xlarge`, `cache.m6g.2xlarge`, `cache.m6g.4xlarge`, `cache.m6g.12xlarge`, `cache.m6g.24xlarge` 

    **M5 node types:** `cache.m5.large`, `cache.m5.xlarge`, `cache.m5.2xlarge`, `cache.m5.4xlarge`, `cache.m5.12xlarge`, `cache.m5.24xlarge` 

    **M4 node types:** `cache.m4.large`, `cache.m4.xlarge`, `cache.m4.2xlarge`, `cache.m4.4xlarge`, `cache.m4.10xlarge`

    **T3 node types:** `cache.t3.micro`, `cache.t3.small`, `cache.t3.medium`

    **T2 node types:** `cache.t2.micro`, `cache.t2.small`, `cache.t2.medium`
  + Previous generation: \(not recommended\)

    **T1 node types:** `cache.t1.micro`

    **M1 node types:** `cache.m1.small`, `cache.m1.medium`, `cache.m1.large`, `cache.m1.xlarge`

    **M3 node types:** `cache.m3.medium`, `cache.m3.large`, `cache.m3.xlarge`, `cache.m3.2xlarge`
+ Compute optimized:
  + Previous generation: \(not recommended\)

    **C1 node types:** `cache.c1.xlarge`
+ Memory optimized:
  + Current generation: 

    **R6g node types:** `cache.r6g.large`, `cache.r6g.xlarge`, `cache.r6g.2xlarge`, `cache.r6g.4xlarge`, `cache.r6g.12xlarge`, `cache.r6g.24xlarge`

    **R5 node types:** `cache.r5.large`, `cache.r5.xlarge`, `cache.r5.2xlarge`, `cache.r5.4xlarge`, `cache.r5.12xlarge`, `cache.r5.24xlarge`

    **R4 node types:** `cache.r4.large`, `cache.r4.xlarge`, `cache.r4.2xlarge`, `cache.r4.4xlarge`, `cache.r4.8xlarge`, `cache.r4.16xlarge`
  + Previous generation: \(not recommended\)

    **M2 node types:** `cache.m2.xlarge`, `cache.m2.2xlarge`, `cache.m2.4xlarge`

    **R3 node types:** `cache.r3.large`, `cache.r3.xlarge`, `cache.r3.2xlarge`, `cache.r3.4xlarge`, `cache.r3.8xlarge`
**Additional node type info**  
+ All current generation instance types are created in Amazon VPC by default\.
+ Redis append\-only files \(AOF\) are not supported for T1 or T2 instances\.
+ Redis Multi\-AZ with automatic failover is not supported on T1 instances\.
+ Redis configuration variables `appendonly` and `appendfsync` are not supported on Redis version 2\.8\.22 and later\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheParameterGroupName`  <a name="cfn-elasticache-cachecluster-cacheparametergroupname"></a>
The name of the parameter group to associate with this cluster\. If this argument is omitted, the default parameter group for the specified engine is used\. You cannot use any parameter group which has `cluster-enabled='yes'` when creating a cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheSecurityGroupNames`  <a name="cfn-elasticache-cachecluster-cachesecuritygroupnames"></a>
A list of security group names to associate with this cluster\.  
Use this parameter only when you are creating a cluster outside of an Amazon Virtual Private Cloud \(Amazon VPC\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheSubnetGroupName`  <a name="cfn-elasticache-cachecluster-cachesubnetgroupname"></a>
The name of the subnet group to be used for the cluster\.  
Use this parameter only when you are creating a cluster in an Amazon Virtual Private Cloud \(Amazon VPC\)\.  
If you're going to launch your cluster in an Amazon VPC, you need to create a subnet group before you start creating a cluster\. For more information, see [AWS::ElastiCache::SubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-subnetgroup.html)\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterName`  <a name="cfn-elasticache-cachecluster-clustername"></a>
A name for the cache cluster\. If you don't specify a name, AWSCloudFormation generates a unique physical ID and uses that ID for the cache cluster\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
The name must contain 1 to 50 alphanumeric characters or hyphens\. The name must start with a letter and cannot end with a hyphen or contain two consecutive hyphens\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Engine`  <a name="cfn-elasticache-cachecluster-engine"></a>
The name of the cache engine to be used for this cluster\.  
Valid values for this parameter are: `memcached` \| `redis`   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-elasticache-cachecluster-engineversion"></a>
The version number of the cache engine to be used for this cluster\. To view the supported cache engine versions, use the DescribeCacheEngineVersions operation\.  
 **Important:** You can upgrade to a newer engine version \(see [Selecting a Cache Engine and Version](https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/SelectEngine.html#VersionManagement)\), but you cannot downgrade to an earlier engine version\. If you want to use an earlier engine version, you must delete the existing cluster or replication group and create it anew with the earlier engine version\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationTopicArn`  <a name="cfn-elasticache-cachecluster-notificationtopicarn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Simple Notification Service \(SNS\) topic to which notifications are sent\.  
The Amazon SNS topic owner must be the same as the cluster owner\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumCacheNodes`  <a name="cfn-elasticache-cachecluster-numcachenodes"></a>
The number of cache nodes that the cache cluster should have\.  
However, if the `PreferredAvailabilityZone` and `PreferredAvailabilityZones `properties were not previously specified and you don't specify any new values, an update requires [ replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)\. 
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Port`  <a name="cfn-elasticache-cachecluster-port"></a>
The port number on which each of the cache nodes accepts connections\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreferredAvailabilityZone`  <a name="cfn-elasticache-cachecluster-preferredavailabilityzone"></a>
The EC2 Availability Zone in which the cluster is created\.  
All nodes belonging to this cluster are placed in the preferred Availability Zone\. If you want to create your nodes across multiple Availability Zones, use `PreferredAvailabilityZones`\.  
Default: System chosen Availability Zone\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PreferredAvailabilityZones`  <a name="cfn-elasticache-cachecluster-preferredavailabilityzones"></a>
A list of the Availability Zones in which cache nodes are created\. The order of the zones in the list is not important\.  
This option is only supported on Memcached\.  
If you are creating your cluster in an Amazon VPC \(recommended\) you can only locate nodes in Availability Zones that are associated with the subnets in the selected subnet group\.  
The number of Availability Zones listed must equal the value of `NumCacheNodes`\.
If you want all the nodes in the same Availability Zone, use `PreferredAvailabilityZone` instead, or repeat the Availability Zone multiple times in the list\.  
Default: System chosen Availability Zones\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-elasticache-cachecluster-preferredmaintenancewindow"></a>
Specifies the weekly time range during which maintenance on the cluster is performed\. It is specified as a range in the format ddd:hh24:mi\-ddd:hh24:mi \(24H Clock UTC\)\. The minimum maintenance window is a 60 minute period\. Valid values for `ddd` are:  
Specifies the weekly time range during which maintenance on the cluster is performed\. It is specified as a range in the format ddd:hh24:mi\-ddd:hh24:mi \(24H Clock UTC\)\. The minimum maintenance window is a 60 minute period\.  
Valid values for `ddd` are:  
+  `sun` 
+  `mon` 
+  `tue` 
+  `wed` 
+  `thu` 
+  `fri` 
+  `sat` 
Example: `sun:23:00-mon:01:30`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotArns`  <a name="cfn-elasticache-cachecluster-snapshotarns"></a>
A single\-element string list containing an Amazon Resource Name \(ARN\) that uniquely identifies a Redis RDB snapshot file stored in Amazon S3\. The snapshot file is used to populate the node group \(shard\)\. The Amazon S3 object name in the ARN cannot contain any commas\.  
This parameter is only valid if the `Engine` parameter is `redis`\.
Example of an Amazon S3 ARN: `arn:aws:s3:::my_bucket/snapshot1.rdb`   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotName`  <a name="cfn-elasticache-cachecluster-snapshotname"></a>
The name of a Redis snapshot from which to restore data into the new node group \(shard\)\. The snapshot status changes to `restoring` while the new node group \(shard\) is being created\.  
This parameter is only valid if the `Engine` parameter is `redis`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotRetentionLimit`  <a name="cfn-elasticache-cachecluster-snapshotretentionlimit"></a>
The number of days for which ElastiCache retains automatic snapshots before deleting them\. For example, if you set `SnapshotRetentionLimit` to 5, a snapshot taken today is retained for 5 days before being deleted\.  
This parameter is only valid if the `Engine` parameter is `redis`\.
Default: 0 \(i\.e\., automatic backups are disabled for this cache cluster\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnapshotWindow`  <a name="cfn-elasticache-cachecluster-snapshotwindow"></a>
The daily time range \(in UTC\) during which ElastiCache begins taking a daily snapshot of your node group \(shard\)\.  
Example: `05:00-09:00`   
If you do not specify this parameter, ElastiCache automatically chooses an appropriate time range\.  
This parameter is only valid if the `Engine` parameter is `redis`\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-elasticache-cachecluster-tags"></a>
A list of cost allocation tags to be added to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-elasticache-cachecluster-vpcsecuritygroupids"></a>
One or more VPC security groups associated with the cluster\.  
Use this parameter only when you are creating a cluster in an Amazon Virtual Private Cloud \(Amazon VPC\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-elasticache-cache-cluster-return-values"></a>

### Ref<a name="aws-properties-elasticache-cache-cluster-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-elasticache-cache-cluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.



#### <a name="aws-properties-elasticache-cache-cluster-return-values-fn--getatt-fn--getatt"></a>

`ConfigurationEndpoint.Address`  <a name="ConfigurationEndpoint.Address-fn::getatt"></a>
 The DNS hostname of the cache node\.  
Redis \(cluster mode disabled\) replication groups don't have this attribute\. Therefore, `Fn::GetAtt` returns a value for this attribute only if the replication group is clustered\. Otherwise, `Fn::GetAtt` fails\.

`ConfigurationEndpoint.Port`  <a name="ConfigurationEndpoint.Port-fn::getatt"></a>
The port number of the configuration endpoint for the Memcached cache cluster\.

`RedisEndpoint.Address`  <a name="RedisEndpoint.Address-fn::getatt"></a>
The DNS address of the configuration endpoint for the Redis cache cluster\.

`RedisEndpoint.Port`  <a name="RedisEndpoint.Port-fn::getatt"></a>
The port number of the configuration endpoint for the Redis cache cluster\.

## Examples<a name="aws-properties-elasticache-cache-cluster--examples"></a>



### Cluster in a Default VPC<a name="aws-properties-elasticache-cache-cluster--examples--Cluster_in_a_Default_VPC"></a>

The following snippet describes an Elasticache cluster in a security group that is in a [default VPC](https://docs.aws.amazon.com/vpc/latest/userguide/default-vpc.html)\. Usually, a security group in a VPC requires the VPC ID to be specified\. In this case, no VPC ID is needed because the security group uses the default VPC\. If you want to specify a VPC for the security group, specify its `VpcId` property\.

For the cache cluster, the `VpcSecurityGroupIds` property is used to associate the cluster with the security group\. Because the `VpcSecurityGroupIds` property requires security group IDs \(not security group names\), the template snippet uses the `Fn::GetAtt` function instead of a `Ref` function on the `ElasticacheSecurityGroup` resource\. The `Ref` function will return the security group name\. If you specify a VPC ID for the security group, `Ref` returns the security group ID\.

 Note that `InstanceSecurityGroup` refers to the logical name of a security group that is not actually defined in this example\. To learn more about the `SourceSecurityGroupName` property, see [AWS::EC2::SecurityGroupIngress](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group-ingress.html)\. 

#### JSON<a name="aws-properties-elasticache-cache-cluster--examples--Cluster_in_a_Default_VPC--json"></a>

```
{
    "ElasticacheSecurityGroup": {
        "Type": "AWS::EC2::SecurityGroup",
        "Properties": {
            "GroupDescription": "Elasticache Security Group",
            "SecurityGroupIngress": [
                {
                    "IpProtocol": "tcp",
                    "FromPort": "11211",
                    "ToPort": "11211",
                    "SourceSecurityGroupName": {
                        "Ref": "InstanceSecurityGroup"
                    }
                }
            ]
        }
    },
    "ElasticacheCluster": {
        "Type": "AWS::ElastiCache::CacheCluster",
        "Properties": {
            "AutoMinorVersionUpgrade": "true",
            "Engine": "memcached",
            "CacheNodeType": "cache.t2.micro",
            "NumCacheNodes": "1",
            "VpcSecurityGroupIds": [
                {
                    "Fn::GetAtt": [
                        "ElasticacheSecurityGroup",
                        "GroupId"
                    ]
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-properties-elasticache-cache-cluster--examples--Cluster_in_a_Default_VPC--yaml"></a>

```
ElasticacheSecurityGroup:
  Type: 'AWS::EC2::SecurityGroup'
  Properties:
    GroupDescription: Elasticache Security Group
    SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: '11211'
        ToPort: '11211'
        SourceSecurityGroupName: !Ref InstanceSecurityGroup
ElasticacheCluster:
  Type: 'AWS::ElastiCache::CacheCluster'
  Properties:
    AutoMinorVersionUpgrade: 'true'
    Engine: memcached
    CacheNodeType: cache.t2.micro
    NumCacheNodes: '1'
    VpcSecurityGroupIds:
      - !GetAtt 
        - ElasticacheSecurityGroup
        - GroupId
```

### Memcached Nodes in Multiple Availability Zones<a name="aws-properties-elasticache-cache-cluster--examples--Memcached_Nodes_in_Multiple_Availability_Zones"></a>

The following example launches a cache cluster with three nodes, where two nodes are created in us\-west\-2a and one is created in us\-west\-2b\. 

#### JSON<a name="aws-properties-elasticache-cache-cluster--examples--Memcached_Nodes_in_Multiple_Availability_Zones--json"></a>

```
{
    "myCacheCluster": {
        "Type": "AWS::ElastiCache::CacheCluster",
        "Properties": {
            "AZMode": "cross-az",
            "CacheNodeType": "cache.m3.medium",
            "Engine": "memcached",
            "NumCacheNodes": "3",
            "PreferredAvailabilityZones": [
                "us-west-2a",
                "us-west-2a",
                "us-west-2b"
            ]
        }
    }
}
```

#### YAML<a name="aws-properties-elasticache-cache-cluster--examples--Memcached_Nodes_in_Multiple_Availability_Zones--yaml"></a>

```
myCacheCluster:
  Type: 'AWS::ElastiCache::CacheCluster'
  Properties:
    AZMode: cross-az
    CacheNodeType: cache.m3.medium
    Engine: memcached
    NumCacheNodes: '3'
    PreferredAvailabilityZones:
      - us-west-2a
      - us-west-2a
      - us-west-2b
```

## See also<a name="aws-properties-elasticache-cache-cluster--seealso"></a>
+ [CreateCacheParameterGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_CreateCacheParameterGroup.html) in the * Amazon ElastiCache API Reference Guide* 
+ [ModifyCacheParameterGroup](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_ModifyCacheParameterGroup.html) in the * Amazon ElastiCache API Reference Guide* 