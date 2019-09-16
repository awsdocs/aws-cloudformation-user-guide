# AWS::Elasticsearch::Domain NodeToNodeEncryptionOptions<a name="aws-properties-elasticsearch-domain-nodetonodeencryptionoptions"></a>

Specifies whether node\-to\-node encryption is enabled\.

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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)