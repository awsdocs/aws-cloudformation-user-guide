# Elasticsearch Domain NodeToNodeEncryptionOptions<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions"></a>

<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions-description"></a>The `NodeToNodeEncryptionOptions` property type specifies whether node\-to\-node encryption is enabled\.

<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions-inheritance"></a> `NodeToNodeEncryptionOptions` is a property of the [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md) resource type\.

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
Specifies whether node\-to\-node encryption is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 