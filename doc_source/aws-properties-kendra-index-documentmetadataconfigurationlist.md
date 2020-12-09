# AWS::Kendra::Index DocumentMetadataConfigurationList<a name="aws-properties-kendra-index-documentmetadataconfigurationlist"></a>

A list of properties associated with a custom index field\.

## Syntax<a name="aws-properties-kendra-index-documentmetadataconfigurationlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-index-documentmetadataconfigurationlist-syntax.json"></a>

```
{
  "[DocumentMetadataConfigurationList](#cfn-kendra-index-documentmetadataconfigurationlist-documentmetadataconfigurationlist)" : [ DocumentMetadataConfiguration, ... ]
}
```

### YAML<a name="aws-properties-kendra-index-documentmetadataconfigurationlist-syntax.yaml"></a>

```
  [DocumentMetadataConfigurationList](#cfn-kendra-index-documentmetadataconfigurationlist-documentmetadataconfigurationlist): 
    - DocumentMetadataConfiguration
```

## Properties<a name="aws-properties-kendra-index-documentmetadataconfigurationlist-properties"></a>

`DocumentMetadataConfigurationList`  <a name="cfn-kendra-index-documentmetadataconfigurationlist-documentmetadataconfigurationlist"></a>
A list of properties associated with a custom index field\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-index-documentmetadataconfigurationlist) of [DocumentMetadataConfiguration](aws-properties-kendra-index-documentmetadataconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)