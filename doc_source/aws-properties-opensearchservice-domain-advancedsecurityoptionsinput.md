# AWS::OpenSearchService::Domain AdvancedSecurityOptionsInput<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput"></a>

Specifies options for fine\-grained access control\.

## Syntax<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-syntax.json"></a>

```
{
  "[Enabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-enabled)" : Boolean,
  "[InternalUserDatabaseEnabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled)" : Boolean,
  "[MasterUserOptions](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-masteruseroptions)" : MasterUserOptions
}
```

### YAML<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-syntax.yaml"></a>

```
  [Enabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-enabled): Boolean
  [InternalUserDatabaseEnabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled): Boolean
  [MasterUserOptions](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-masteruseroptions): 
    MasterUserOptions
```

## Properties<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-properties"></a>

`Enabled`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-enabled"></a>
True to enable fine\-grained access control\. You must also enable encryption of data at rest and node\-to\-node encryption\. See [Fine\-grained access control in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/fgac.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InternalUserDatabaseEnabled`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled"></a>
True to enable the internal user database\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserOptions`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-masteruseroptions"></a>
Specifies information about the master user\.  
*Required*: No  
*Type*: [MasterUserOptions](aws-properties-opensearchservice-domain-masteruseroptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)