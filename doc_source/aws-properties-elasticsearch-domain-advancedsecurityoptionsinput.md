# AWS::Elasticsearch::Domain AdvancedSecurityOptionsInput<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput"></a>

Specifies options for fine\-grained access control\.

**Important**  
The `AWS::Elasticsearch::Domain` resource is being replaced by the [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html) resource\. While the legacy Elasticsearch resource and options are still supported, we recommend modifying your existing Cloudformation templates to use the new OpenSearch Service resource, which supports both OpenSearch and Elasticsearch\. For more information about the service rename, see [New resource types](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/rename.html#rename-resource) in the *Amazon OpenSearch Service Developer Guide*\.

## Syntax<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-syntax.json"></a>

```
{
  "[AnonymousAuthEnabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-anonymousauthenabled)" : Boolean,
  "[Enabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-enabled)" : Boolean,
  "[InternalUserDatabaseEnabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled)" : Boolean,
  "[MasterUserOptions](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-masteruseroptions)" : MasterUserOptions
}
```

### YAML<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-syntax.yaml"></a>

```
  [AnonymousAuthEnabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-anonymousauthenabled): Boolean
  [Enabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-enabled): Boolean
  [InternalUserDatabaseEnabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled): Boolean
  [MasterUserOptions](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-masteruseroptions): 
    MasterUserOptions
```

## Properties<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-properties"></a>

`AnonymousAuthEnabled`  <a name="cfn-elasticsearch-domain-advancedsecurityoptionsinput-anonymousauthenabled"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-elasticsearch-domain-advancedsecurityoptionsinput-enabled"></a>
True to enable fine\-grained access control\. You must also enable encryption of data at rest and node\-to\-node encryption\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InternalUserDatabaseEnabled`  <a name="cfn-elasticsearch-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled"></a>
True to enable the internal user database\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserOptions`  <a name="cfn-elasticsearch-domain-advancedsecurityoptionsinput-masteruseroptions"></a>
Specifies information about the master user\.  
*Required*: No  
*Type*: [MasterUserOptions](aws-properties-elasticsearch-domain-masteruseroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)