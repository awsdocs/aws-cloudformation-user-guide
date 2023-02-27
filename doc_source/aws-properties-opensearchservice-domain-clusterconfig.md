# AWS::OpenSearchService::Domain ClusterConfig<a name="aws-properties-opensearchservice-domain-clusterconfig"></a>

The cluster configuration for the OpenSearch Service domain\. You can specify options such as the instance type and the number of instances\. For more information, see [Creating and managing Amazon OpenSearch Service domains](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/createupdatedomains.html) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-opensearchservice-domain-clusterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-clusterconfig-syntax.json"></a>

```
{
  "[DedicatedMasterCount](#cfn-opensearchservice-domain-clusterconfig-dedicatedmastercount)" : Integer,
  "[DedicatedMasterEnabled](#cfn-opensearchservice-domain-clusterconfig-dedicatedmasterenabled)" : Boolean,
  "[DedicatedMasterType](#cfn-opensearchservice-domain-clusterconfig-dedicatedmastertype)" : String,
  "[InstanceCount](#cfn-opensearchservice-domain-clusterconfig-instancecount)" : Integer,
  "[InstanceType](#cfn-opensearchservice-domain-clusterconfig-instancetype)" : String,
  "[WarmCount](#cfn-opensearchservice-domain-clusterconfig-warmcount)" : Integer,
  "[WarmEnabled](#cfn-opensearchservice-domain-clusterconfig-warmenabled)" : Boolean,
  "[WarmType](#cfn-opensearchservice-domain-clusterconfig-warmtype)" : String,
  "[ZoneAwarenessConfig](#cfn-opensearchservice-domain-clusterconfig-zoneawarenessconfig)" : ZoneAwarenessConfig,
  "[ZoneAwarenessEnabled](#cfn-opensearchservice-domain-clusterconfig-zoneawarenessenabled)" : Boolean
}
```

### YAML<a name="aws-properties-opensearchservice-domain-clusterconfig-syntax.yaml"></a>

```
  [DedicatedMasterCount](#cfn-opensearchservice-domain-clusterconfig-dedicatedmastercount): Integer
  [DedicatedMasterEnabled](#cfn-opensearchservice-domain-clusterconfig-dedicatedmasterenabled): Boolean
  [DedicatedMasterType](#cfn-opensearchservice-domain-clusterconfig-dedicatedmastertype): String
  [InstanceCount](#cfn-opensearchservice-domain-clusterconfig-instancecount): Integer
  [InstanceType](#cfn-opensearchservice-domain-clusterconfig-instancetype): String
  [WarmCount](#cfn-opensearchservice-domain-clusterconfig-warmcount): Integer
  [WarmEnabled](#cfn-opensearchservice-domain-clusterconfig-warmenabled): Boolean
  [WarmType](#cfn-opensearchservice-domain-clusterconfig-warmtype): String
  [ZoneAwarenessConfig](#cfn-opensearchservice-domain-clusterconfig-zoneawarenessconfig): 
    ZoneAwarenessConfig
  [ZoneAwarenessEnabled](#cfn-opensearchservice-domain-clusterconfig-zoneawarenessenabled): Boolean
```

## Properties<a name="aws-properties-opensearchservice-domain-clusterconfig-properties"></a>

`DedicatedMasterCount`  <a name="cfn-opensearchservice-domain-clusterconfig-dedicatedmastercount"></a>
The number of instances to use for the master node\. If you specify this property, you must specify `true` for the `DedicatedMasterEnabled` property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DedicatedMasterEnabled`  <a name="cfn-opensearchservice-domain-clusterconfig-dedicatedmasterenabled"></a>
Indicates whether to use a dedicated master node for the OpenSearch Service domain\. A dedicated master node is a cluster node that performs cluster management tasks, but doesn't hold data or respond to data upload requests\. Dedicated master nodes offload cluster management tasks to increase the stability of your search clusters\. See [Dedicated master nodes in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/managedomains-dedicatedmasternodes.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DedicatedMasterType`  <a name="cfn-opensearchservice-domain-clusterconfig-dedicatedmastertype"></a>
The hardware configuration of the computer that hosts the dedicated master node, such as `m3.medium.search`\. If you specify this property, you must specify `true` for the `DedicatedMasterEnabled` property\. For valid values, see [Supported instance types in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/supported-instance-types.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `c4.2xlarge.search | c4.4xlarge.search | c4.8xlarge.search | c4.large.search | c4.xlarge.search | c5.18xlarge.search | c5.2xlarge.search | c5.4xlarge.search | c5.9xlarge.search | c5.large.search | c5.xlarge.search | c6g.12xlarge.search | c6g.2xlarge.search | c6g.4xlarge.search | c6g.8xlarge.search | c6g.large.search | c6g.xlarge.search | d2.2xlarge.search | d2.4xlarge.search | d2.8xlarge.search | d2.xlarge.search | i2.2xlarge.search | i2.xlarge.search | i3.16xlarge.search | i3.2xlarge.search | i3.4xlarge.search | i3.8xlarge.search | i3.large.search | i3.xlarge.search | m3.2xlarge.search | m3.large.search | m3.medium.search | m3.xlarge.search | m4.10xlarge.search | m4.2xlarge.search | m4.4xlarge.search | m4.large.search | m4.xlarge.search | m5.12xlarge.search | m5.24xlarge.search | m5.2xlarge.search | m5.4xlarge.search | m5.large.search | m5.xlarge.search | m6g.12xlarge.search | m6g.2xlarge.search | m6g.4xlarge.search | m6g.8xlarge.search | m6g.large.search | m6g.xlarge.search | r3.2xlarge.search | r3.4xlarge.search | r3.8xlarge.search | r3.large.search | r3.xlarge.search | r4.16xlarge.search | r4.2xlarge.search | r4.4xlarge.search | r4.8xlarge.search | r4.large.search | r4.xlarge.search | r5.12xlarge.search | r5.24xlarge.search | r5.2xlarge.search | r5.4xlarge.search | r5.large.search | r5.xlarge.search | r6g.12xlarge.search | r6g.2xlarge.search | r6g.4xlarge.search | r6g.8xlarge.search | r6g.large.search | r6g.xlarge.search | r6gd.12xlarge.search | r6gd.16xlarge.search | r6gd.2xlarge.search | r6gd.4xlarge.search | r6gd.8xlarge.search | r6gd.large.search | r6gd.xlarge.search | t2.medium.search | t2.micro.search | t2.small.search | t3.2xlarge.search | t3.large.search | t3.medium.search | t3.micro.search | t3.nano.search | t3.small.search | t3.xlarge.search | t4g.medium.search | t4g.small.search | ultrawarm1.large.search | ultrawarm1.medium.search | ultrawarm1.xlarge.search`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceCount`  <a name="cfn-opensearchservice-domain-clusterconfig-instancecount"></a>
The number of data nodes \(instances\) to use in the OpenSearch Service domain\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-opensearchservice-domain-clusterconfig-instancetype"></a>
The instance type for your data nodes, such as `m3.medium.search`\. For valid values, see [Supported instance types in Amazon OpenSearch Service ](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/supported-instance-types.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `c4.2xlarge.search | c4.4xlarge.search | c4.8xlarge.search | c4.large.search | c4.xlarge.search | c5.18xlarge.search | c5.2xlarge.search | c5.4xlarge.search | c5.9xlarge.search | c5.large.search | c5.xlarge.search | c6g.12xlarge.search | c6g.2xlarge.search | c6g.4xlarge.search | c6g.8xlarge.search | c6g.large.search | c6g.xlarge.search | d2.2xlarge.search | d2.4xlarge.search | d2.8xlarge.search | d2.xlarge.search | i2.2xlarge.search | i2.xlarge.search | i3.16xlarge.search | i3.2xlarge.search | i3.4xlarge.search | i3.8xlarge.search | i3.large.search | i3.xlarge.search | m3.2xlarge.search | m3.large.search | m3.medium.search | m3.xlarge.search | m4.10xlarge.search | m4.2xlarge.search | m4.4xlarge.search | m4.large.search | m4.xlarge.search | m5.12xlarge.search | m5.24xlarge.search | m5.2xlarge.search | m5.4xlarge.search | m5.large.search | m5.xlarge.search | m6g.12xlarge.search | m6g.2xlarge.search | m6g.4xlarge.search | m6g.8xlarge.search | m6g.large.search | m6g.xlarge.search | r3.2xlarge.search | r3.4xlarge.search | r3.8xlarge.search | r3.large.search | r3.xlarge.search | r4.16xlarge.search | r4.2xlarge.search | r4.4xlarge.search | r4.8xlarge.search | r4.large.search | r4.xlarge.search | r5.12xlarge.search | r5.24xlarge.search | r5.2xlarge.search | r5.4xlarge.search | r5.large.search | r5.xlarge.search | r6g.12xlarge.search | r6g.2xlarge.search | r6g.4xlarge.search | r6g.8xlarge.search | r6g.large.search | r6g.xlarge.search | r6gd.12xlarge.search | r6gd.16xlarge.search | r6gd.2xlarge.search | r6gd.4xlarge.search | r6gd.8xlarge.search | r6gd.large.search | r6gd.xlarge.search | t2.medium.search | t2.micro.search | t2.small.search | t3.2xlarge.search | t3.large.search | t3.medium.search | t3.micro.search | t3.nano.search | t3.small.search | t3.xlarge.search | t4g.medium.search | t4g.small.search | ultrawarm1.large.search | ultrawarm1.medium.search | ultrawarm1.xlarge.search`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WarmCount`  <a name="cfn-opensearchservice-domain-clusterconfig-warmcount"></a>
The number of warm nodes in the cluster\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WarmEnabled`  <a name="cfn-opensearchservice-domain-clusterconfig-warmenabled"></a>
Whether to enable UltraWarm storage for the cluster\. See [UltraWarm storage for Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ultrawarm.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WarmType`  <a name="cfn-opensearchservice-domain-clusterconfig-warmtype"></a>
The instance type for the cluster's warm nodes\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ultrawarm1.large.search | ultrawarm1.medium.search | ultrawarm1.xlarge.search`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ZoneAwarenessConfig`  <a name="cfn-opensearchservice-domain-clusterconfig-zoneawarenessconfig"></a>
Specifies zone awareness configuration options\. Only use if `ZoneAwarenessEnabled` is `true`\.  
*Required*: No  
*Type*: [ZoneAwarenessConfig](aws-properties-opensearchservice-domain-zoneawarenessconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ZoneAwarenessEnabled`  <a name="cfn-opensearchservice-domain-clusterconfig-zoneawarenessenabled"></a>
Indicates whether to enable zone awareness for the OpenSearch Service domain\. When you enable zone awareness, OpenSearch Service allocates the nodes and replica index shards that belong to a cluster across two Availability Zones \(AZs\) in the same region to prevent data loss and minimize downtime in the event of node or data center failure\. Don't enable zone awareness if your cluster has no replica index shards or is a single\-node cluster\. For more information, see [Configuring a multi\-AZ domain in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/managedomains-multiaz.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)