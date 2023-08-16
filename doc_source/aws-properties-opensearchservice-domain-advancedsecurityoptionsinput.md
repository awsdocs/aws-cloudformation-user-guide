# AWS::OpenSearchService::Domain AdvancedSecurityOptionsInput<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput"></a>

Specifies options for fine\-grained access control\.

If you specify advanced security options, you must also enable node\-to\-node encryption \([NodeToNodeEncryptionOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opensearchservice-domain-nodetonodeencryptionoptions.html)\) and encryption at rest \([EncryptionAtRestOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opensearchservice-domain-encryptionatrestoptions.html)\)\. You must also enable `EnforceHTTPS` within [DomainEndpointOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opensearchservice-domain-domainendpointoptions.html), which requires HTTPS for all traffic to the domain\.

## Syntax<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-syntax.json"></a>

```
{
  "[AnonymousAuthDisableDate](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-anonymousauthdisabledate)" : String,
  "[AnonymousAuthEnabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-anonymousauthenabled)" : Boolean,
  "[Enabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-enabled)" : Boolean,
  "[InternalUserDatabaseEnabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled)" : Boolean,
  "[MasterUserOptions](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-masteruseroptions)" : MasterUserOptions,
  "[SAMLOptions](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-samloptions)" : SAMLOptions
}
```

### YAML<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-syntax.yaml"></a>

```
  [AnonymousAuthDisableDate](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-anonymousauthdisabledate): String
  [AnonymousAuthEnabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-anonymousauthenabled): Boolean
  [Enabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-enabled): Boolean
  [InternalUserDatabaseEnabled](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled): Boolean
  [MasterUserOptions](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-masteruseroptions): 
    MasterUserOptions
  [SAMLOptions](#cfn-opensearchservice-domain-advancedsecurityoptionsinput-samloptions): 
    SAMLOptions
```

## Properties<a name="aws-properties-opensearchservice-domain-advancedsecurityoptionsinput-properties"></a>

`AnonymousAuthDisableDate`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-anonymousauthdisabledate"></a>
Date and time when the migration period will be disabled\. Only necessary when [enabling fine\-grained access control on an existing domain](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/fgac.html#fgac-enabling-existing)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AnonymousAuthEnabled`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-anonymousauthenabled"></a>
True to enable a 30\-day migration period during which administrators can create role mappings\. Only necessary when [enabling fine\-grained access control on an existing domain](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/fgac.html#fgac-enabling-existing)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-enabled"></a>
True to enable fine\-grained access control\. You must also enable encryption of data at rest and node\-to\-node encryption\. See [Fine\-grained access control in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/fgac.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InternalUserDatabaseEnabled`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled"></a>
True to enable the internal user database\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserOptions`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-masteruseroptions"></a>
Specifies information about the master user\.  
*Required*: No  
*Type*: [MasterUserOptions](aws-properties-opensearchservice-domain-masteruseroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SAMLOptions`  <a name="cfn-opensearchservice-domain-advancedsecurityoptionsinput-samloptions"></a>
Container for information about the SAML configuration for OpenSearch Dashboards\.  
*Required*: No  
*Type*: [SAMLOptions](aws-properties-opensearchservice-domain-samloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)