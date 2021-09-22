# AWS::Elasticsearch::Domain ColdStorageOptions<a name="aws-properties-elasticsearch-domain-coldstorageoptions"></a>

Specifies options for cold storage\. For more information, see [Cold storage for Amazon Elasticsearch Service](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/cold-storage.html)\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-elasticsearch-domain-coldstorageoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-coldstorageoptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-elasticsearch-domain-coldstorageoptions-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-elasticsearch-domain-coldstorageoptions-syntax.yaml"></a>

```
  [Enabled](#cfn-elasticsearch-domain-coldstorageoptions-enabled): Boolean
```

## Properties<a name="aws-properties-elasticsearch-domain-coldstorageoptions-properties"></a>

`Enabled`  <a name="cfn-elasticsearch-domain-coldstorageoptions-enabled"></a>
Whether to enable or disable cold storage on the domain\. You must enable UltraWarm storage in order to enable cold storage\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)