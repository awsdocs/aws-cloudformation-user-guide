# AWS::Elasticsearch::Domain EncryptionAtRestOptions<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions"></a>

Whether the domain should encrypt data at rest, and if so, the AWS Key Management Service \(KMS\) key to use\. Can only be used to create a new domain, not update an existing one\.

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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-elasticsearch-domain-encryptionatrestoptions-kmskeyid"></a>
The KMS key ID\. Takes the form `1a2a3a4-1a2a-3a4a-5a6a-1a2a3a4a5a6a`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions--seealso"></a>
+ [CreateElasticsearchDomain](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-actions-createelasticsearchdomain) in the *Amazon Elasticsearch Service Developer Guide*\.

