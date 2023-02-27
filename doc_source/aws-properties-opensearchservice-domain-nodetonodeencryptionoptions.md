# AWS::OpenSearchService::Domain NodeToNodeEncryptionOptions<a name="aws-properties-opensearchservice-domain-nodetonodeencryptionoptions"></a>

Specifies options for node\-to\-node encryption\.

## Syntax<a name="aws-properties-opensearchservice-domain-nodetonodeencryptionoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-nodetonodeencryptionoptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-opensearchservice-domain-nodetonodeencryptionoptions-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-opensearchservice-domain-nodetonodeencryptionoptions-syntax.yaml"></a>

```
  [Enabled](#cfn-opensearchservice-domain-nodetonodeencryptionoptions-enabled): Boolean
```

## Properties<a name="aws-properties-opensearchservice-domain-nodetonodeencryptionoptions-properties"></a>

`Enabled`  <a name="cfn-opensearchservice-domain-nodetonodeencryptionoptions-enabled"></a>
Specifies to enable or disable node\-to\-node encryption on the domain\. Required if you enable fine\-grained access control in [AdvancedSecurityOptionsInput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opensearchservice-domain-advancedsecurityoptionsinput.html)\.  
*Required*: Conditional  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)