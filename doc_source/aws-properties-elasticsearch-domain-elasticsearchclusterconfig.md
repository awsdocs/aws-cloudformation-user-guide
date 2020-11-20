# AWS::Elasticsearch::Domain ElasticsearchClusterConfig<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig"></a>

The cluster configuration for the Amazon ES domain\. You can specify options such as the instance type and the number of instances\. For more information, see [Configuring Amazon ES Domains](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains-configure-cluster-cli) in the *Amazon Elasticsearch Service Developer Guide*\.

## Syntax<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-syntax.json"></a>

```
{
  "[DedicatedMasterCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount)" : Integer,
  "[DedicatedMasterEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled)" : Boolean,
  "[DedicatedMasterType](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype)" : String,
  "[InstanceCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount)" : Integer,
  "[InstanceType](#cfn-elasticsearch-domain-elasticseachclusterconfig-instnacetype)" : String,
  "[WarmCount](#cfn-elasticsearch-domain-elasticsearchclusterconfig-warmcount)" : Integer,
  "[WarmEnabled](#cfn-elasticsearch-domain-elasticsearchclusterconfig-warmenabled)" : Boolean,
  "[WarmType](#cfn-elasticsearch-domain-elasticsearchclusterconfig-warmtype)" : String,
  "[ZoneAwarenessConfig](#cfn-elasticsearch-domain-elasticsearchclusterconfig-zoneawarenessconfig)" : ZoneAwarenessConfig,
  "[ZoneAwarenessEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled)" : Boolean
}
```

### YAML<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-syntax.yaml"></a>

```
  [DedicatedMasterCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount): Integer
  [DedicatedMasterEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled): Boolean
  [DedicatedMasterType](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype): String
  [InstanceCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount): Integer
  [InstanceType](#cfn-elasticsearch-domain-elasticseachclusterconfig-instnacetype): String
  [WarmCount](#cfn-elasticsearch-domain-elasticsearchclusterconfig-warmcount): Integer
  [WarmEnabled](#cfn-elasticsearch-domain-elasticsearchclusterconfig-warmenabled): Boolean
  [WarmType](#cfn-elasticsearch-domain-elasticsearchclusterconfig-warmtype): String
  [ZoneAwarenessConfig](#cfn-elasticsearch-domain-elasticsearchclusterconfig-zoneawarenessconfig): 
    ZoneAwarenessConfig
  [ZoneAwarenessEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled): Boolean
```

## Properties<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-properties"></a>

`DedicatedMasterCount`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount"></a>
The number of instances to use for the master node\. If you specify this property, you must specify true for the DedicatedMasterEnabled property\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DedicatedMasterEnabled`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled"></a>
Indicates whether to use a dedicated master node for the Amazon ES domain\. A dedicated master node is a cluster node that performs cluster management tasks, but doesn't hold data or respond to data upload requests\. Dedicated master nodes offload cluster management tasks to increase the stability of your search clusters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DedicatedMasterType`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype"></a>
The hardware configuration of the computer that hosts the dedicated master node, such as `m3.medium.elasticsearch`\. If you specify this property, you must specify true for the `DedicatedMasterEnabled` property\. For valid values, see [Supported Instance Types](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/aes-supported-instance-types.html) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceCount`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount"></a>
The number of data nodes \(instances\) to use in the Amazon ES domain\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-instnacetype"></a>
The instance type for your data nodes, such as `m3.medium.elasticsearch`\. For valid values, see [Supported Instance Types](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/aes-supported-instance-types.html) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WarmCount`  <a name="cfn-elasticsearch-domain-elasticsearchclusterconfig-warmcount"></a>
The number of warm nodes in the cluster\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WarmEnabled`  <a name="cfn-elasticsearch-domain-elasticsearchclusterconfig-warmenabled"></a>
Whether to enable warm storage for the cluster\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WarmType`  <a name="cfn-elasticsearch-domain-elasticsearchclusterconfig-warmtype"></a>
The instance type for the cluster's warm nodes\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ZoneAwarenessConfig`  <a name="cfn-elasticsearch-domain-elasticsearchclusterconfig-zoneawarenessconfig"></a>
Specifies zone awareness configuration options\. Only use if `ZoneAwarenessEnabled` is `true`\.  
*Required*: No  
*Type*: [ZoneAwarenessConfig](aws-properties-elasticsearch-domain-zoneawarenessconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ZoneAwarenessEnabled`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled"></a>
Indicates whether to enable zone awareness for the Amazon ES domain\. When you enable zone awareness, Amazon ES allocates the nodes and replica index shards that belong to a cluster across two Availability Zones \(AZs\) in the same region to prevent data loss and minimize downtime in the event of node or data center failure\. Don't enable zone awareness if your cluster has no replica index shards or is a single\-node cluster\. For more information, see [Configuring a Multi\-AZ Domain](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-managedomains.html#es-managedomains-multiaz) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)