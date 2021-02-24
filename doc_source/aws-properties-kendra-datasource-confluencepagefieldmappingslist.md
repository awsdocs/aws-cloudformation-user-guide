# AWS::Kendra::DataSource ConfluencePageFieldMappingsList<a name="aws-properties-kendra-datasource-confluencepagefieldmappingslist"></a>

Specifies one or more `ConfluencePageToIndexFieldMapping` objects\.

## Syntax<a name="aws-properties-kendra-datasource-confluencepagefieldmappingslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluencepagefieldmappingslist-syntax.json"></a>

```
{
  "[ConfluencePageFieldMappingsList](#cfn-kendra-datasource-confluencepagefieldmappingslist-confluencepagefieldmappingslist)" : [ ConfluencePageToIndexFieldMapping, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-confluencepagefieldmappingslist-syntax.yaml"></a>

```
  [ConfluencePageFieldMappingsList](#cfn-kendra-datasource-confluencepagefieldmappingslist-confluencepagefieldmappingslist): 
    - ConfluencePageToIndexFieldMapping
```

## Properties<a name="aws-properties-kendra-datasource-confluencepagefieldmappingslist-properties"></a>

`ConfluencePageFieldMappingsList`  <a name="cfn-kendra-datasource-confluencepagefieldmappingslist-confluencepagefieldmappingslist"></a>
A list of mappings between Confluence and Amazon Kendra index fields\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-confluencepagefieldmappingslist) of [ConfluencePageToIndexFieldMapping](aws-properties-kendra-datasource-confluencepagetoindexfieldmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)