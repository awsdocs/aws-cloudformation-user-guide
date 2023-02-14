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