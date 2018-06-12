# Amazon Elasticsearch Service Domain EncryptionAtRestOptions<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions"></a>

<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions-description"></a>The `EncryptionAtRestOptions` property type specifies whether the domain should encrypt data at rest, and if so, the AWS Key Management Service \(KMS\) key to use\. Can only be used to create a new domain, not update an existing one\.

<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions-inheritance"></a> `EncryptionAtRestOptions` is a property of the [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md) resource\.

## Syntax<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax.json"></a>

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
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`KmsKeyId`  <a name="cfn-elasticsearch-domain-encryptionatrestoptions-kmskeyid"></a>
The KMS key ID\. Takes the form `1a2a3a4-1a2a-3a4a-5a6a-1a2a3a4a5a6a`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-elasticsearch-domain-encryptionatrestoptions-seealso"></a>
+ [CreateElasticsearchDomain](http://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-actions-createelasticsearchdomain) in the *Amazon Elasticsearch Service Developer Guide*