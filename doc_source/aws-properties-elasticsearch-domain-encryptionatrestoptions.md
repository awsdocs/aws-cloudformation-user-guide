# AWS::Elasticsearch::Domain EncryptionAtRestOptions<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions"></a>

Whether the domain should encrypt data at rest, and if so, the AWS Key Management Service key to use\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-elasticsearch-domain-encryptionatrestoptions-enabled)" : Boolean,
  "[KmsKeyId](#cfn-elasticsearch-domain-encryptionatrestoptions-kmskeyid)" : String
}
```

### YAML<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions-syntax.yaml"></a>

```
  [Enabled](#cfn-elasticsearch-domain-encryptionatrestoptions-enabled): Boolean
  [KmsKeyId](#cfn-elasticsearch-domain-encryptionatrestoptions-kmskeyid): String
```

## Properties<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions-properties"></a>

`Enabled`  <a name="cfn-elasticsearch-domain-encryptionatrestoptions-enabled"></a>
Specify `true` to enable encryption at rest\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`KmsKeyId`  <a name="cfn-elasticsearch-domain-encryptionatrestoptions-kmskeyid"></a>
The KMS key ID\. Takes the form `1a2a3a4-1a2a-3a4a-5a6a-1a2a3a4a5a6a`\. Required if you enable encryption at rest\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions--seealso"></a>
+ [CreateDomain](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/configuration-api.html#configuration-api-actions-createdomain) in the *Amazon OpenSearch Service Developer Guide*\.

