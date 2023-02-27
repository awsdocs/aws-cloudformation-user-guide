# AWS::Elasticsearch::Domain NodeToNodeEncryptionOptions<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions"></a>

Specifies whether node\-to\-node encryption is enabled\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-elasticsearch-domain-nodetonodeencryptionoptions-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions-syntax.yaml"></a>

```
  [Enabled](#cfn-elasticsearch-domain-nodetonodeencryptionoptions-enabled): Boolean
```

## Properties<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions-properties"></a>

`Enabled`  <a name="cfn-elasticsearch-domain-nodetonodeencryptionoptions-enabled"></a>
Specifies whether node\-to\-node encryption is enabled, as a Boolean\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)