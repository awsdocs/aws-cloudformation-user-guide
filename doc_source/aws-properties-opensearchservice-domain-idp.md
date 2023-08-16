# AWS::OpenSearchService::Domain Idp<a name="aws-properties-opensearchservice-domain-idp"></a>

The SAML Identity Provider's information\.

## Syntax<a name="aws-properties-opensearchservice-domain-idp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-idp-syntax.json"></a>

```
{
  "[EntityId](#cfn-opensearchservice-domain-idp-entityid)" : String,
  "[MetadataContent](#cfn-opensearchservice-domain-idp-metadatacontent)" : String
}
```

### YAML<a name="aws-properties-opensearchservice-domain-idp-syntax.yaml"></a>

```
  [EntityId](#cfn-opensearchservice-domain-idp-entityid): String
  [MetadataContent](#cfn-opensearchservice-domain-idp-metadatacontent): String
```

## Properties<a name="aws-properties-opensearchservice-domain-idp-properties"></a>

`EntityId`  <a name="cfn-opensearchservice-domain-idp-entityid"></a>
The unique entity ID of the application in the SAML identity provider\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `8`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetadataContent`  <a name="cfn-opensearchservice-domain-idp-metadatacontent"></a>
The metadata of the SAML application, in XML format\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1048576`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)