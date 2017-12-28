# Amazon Elasticsearch Service Domain ElasticsearchClusterConfig<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig"></a>

`ElasticsearchClusterConfig` is a property of the [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md) resource that configures the cluster of an Amazon Elasticsearch Service \(Amazon ES\) domain\.

## Syntax<a name="w3ab2c21c14d857b5"></a>

### JSON<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount)" : Integer,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancetype)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled)" : Boolean
}
```

### YAML<a name="aws-properties-elasticsearch-domain-elasticsearchclusterconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastercount): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmasterenabled): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-dedicatedmastertype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancecount): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-instancetype): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticsearch-domain-elasticseachclusterconfig-zoneawarenessenabled): Boolean
```

## Properties<a name="w3ab2c21c14d857b7"></a>

`DedicatedMasterCount`  
The number of instances to use for the master node\.  
If you specify this property, you must specify `true` for the `DedicatedMasterEnabled` property  
*Required: *No  
*Type*: Integer

`DedicatedMasterEnabled`  
Indicates whether to use a dedicated master node for the Amazon ES domain\. A dedicated master node is a cluster node that performs cluster management tasks, but doesn't hold data or respond to data upload requests\. Dedicated master nodes offload cluster management tasks to increase the stability of your search clusters\.  
*Required: *No  
*Type*: Boolean

`DedicatedMasterType`  
The hardware configuration of the computer that hosts the dedicated master node, such as `m3.medium.elasticsearch`\. For valid values, see [Configuring Amazon ES Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains-configure-cluster-cli) in the *Amazon Elasticsearch Service Developer Guide*\.  
If you specify this property, you must specify `true` for the `DedicatedMasterEnabled` property  
*Required: *No  
*Type*: String

`InstanceCount`  
The number of data nodes \(instances\) to use in the Amazon ES domain\.  
*Required: *No  
*Type*: Integer

`InstanceType`  
The instance type for your data nodes, such as `m3.medium.elasticsearch`\. For valid values, see [Configuring Amazon ES Domains](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-createupdatedomains.html#es-createdomains-configure-cluster-cli) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required: *No  
*Type*: String

`ZoneAwarenessEnabled`  
Indicates whether to enable zone awareness for the Amazon ES domain\. When you enable zone awareness, Amazon ES allocates the nodes and replica index shards that belong to a cluster across two Availability Zones \(AZs\) in the same region to prevent data loss and minimize downtime in the event of node or data center failure\. Don't enable zone awareness if your cluster has no replica index shards or is a single\-node cluster\. For more information, see [Enabling Zone Awareness](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-managedomains.html#es-managedomains-zoneawareness) in the *Amazon Elasticsearch Service Developer Guide*\.  
*Required: *No  
*Type*: Boolean