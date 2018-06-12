# Amazon Elasticsearch Service Domain ElasticsearchClusterConfig<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig"></a>

`ElasticsearchClusterConfig` is a property of the [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md) resource that configures the cluster of an Amazon Elasticsearch Service \(Amazon ES\) domain\.

## Syntax<a name="w3ab2c21c14e1044b5"></a>

### JSON<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-syntax.json"></a>

```
{
  "[DedicatedMasterCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount)" : Integer,
  "[DedicatedMasterEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled)" : Boolean,
  "[DedicatedMasterType](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype)" : String,
  "[InstanceCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount)" : Integer,
  "[InstanceType](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancetype)" : String,
  "[ZoneAwarenessEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled)" : Boolean
}
```

### YAML<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-syntax.yaml"></a>

```
[DedicatedMasterCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount): Integer
[DedicatedMasterEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled): Boolean
[DedicatedMasterType](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype): String
[InstanceCount](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount): Integer
[InstanceType](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancetype): String
[ZoneAwarenessEnabled](#cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled): Boolean
```

## Properties<a name="w3ab2c21c14e1044b7"></a>

`DedicatedMasterCount`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount"></a>
The number of instances to use for the master node\.  
If you specify this property, you must specify `true` for the `DedicatedMasterEnabled` property  
*Required*: No  
*Type*: Integer

`DedicatedMasterEnabled`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled"></a>
Indicates whether to use a dedicated master node for the Amazon ES domain\. A dedicated master node is a cluster node that performs cluster management tasks, but doesn't hold data or respond to data upload requests\. Dedicated master nodes offload cluster management tasks to increase the stability of your search clusters\.  
*Required*: No  
*Type*: Boolean

`DedicatedMasterType`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype"></a>
The hardware configuration of the computer that hosts the dedicated master node, such as `m3.medium.elasticsearch`\. For valid values, see [Configuring Amazon ES Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains-configure-cluster-cli) in the *Amazon Elasticsearch Service Developer Guide*\.  
If you specify this property, you must specify `true` for the `DedicatedMasterEnabled` property  
*Required*: No  
*Type*: String

`InstanceCount`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount"></a>
The number of data nodes \(instances\) to use in the Amazon ES domain\.  
*Required*: No  
*Type*: Integer

`InstanceType`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-instancetype"></a>
The instance type for your data nodes, such as `m3.medium.elasticsearch`\. For valid values, see [Configuring Amazon ES Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains-configure-cluster-cli) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: String

`ZoneAwarenessEnabled`  <a name="cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled"></a>
Indicates whether to enable zone awareness for the Amazon ES domain\. When you enable zone awareness, Amazon ES allocates the nodes and replica index shards that belong to a cluster across two Availability Zones \(AZs\) in the same region to prevent data loss and minimize downtime in the event of node or data center failure\. Don't enable zone awareness if your cluster has no replica index shards or is a single\-node cluster\. For more information, see [Enabling Zone Awareness](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-managedomains.html#es-managedomains-zoneawareness) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required*: No  
*Type*: Boolean