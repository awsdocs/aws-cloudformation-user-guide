# AWS::Kendra::DataSource ConfluenceBlogFieldMappingsList<a name="aws-properties-kendra-datasource-confluenceblogfieldmappingslist"></a>

Specifies one or more `ConfluenceBlogToIndexFieldMapping` objects\.

## Syntax<a name="aws-properties-kendra-datasource-confluenceblogfieldmappingslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluenceblogfieldmappingslist-syntax.json"></a>

```
{
  "[ConfluenceBlogFieldMappingsList](#cfn-kendra-datasource-confluenceblogfieldmappingslist-confluenceblogfieldmappingslist)" : [ ConfluenceBlogToIndexFieldMapping, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-confluenceblogfieldmappingslist-syntax.yaml"></a>

```
  [ConfluenceBlogFieldMappingsList](#cfn-kendra-datasource-confluenceblogfieldmappingslist-confluenceblogfieldmappingslist): 
    - ConfluenceBlogToIndexFieldMapping
```

## Properties<a name="aws-properties-kendra-datasource-confluenceblogfieldmappingslist-properties"></a>

`ConfluenceBlogFieldMappingsList`  <a name="cfn-kendra-datasource-confluenceblogfieldmappingslist-confluenceblogfieldmappingslist"></a>
A list of mappings between Confluence and Amazon Kendra index fields\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-confluenceblogfieldmappingslist) of [ConfluenceBlogToIndexFieldMapping](aws-properties-kendra-datasource-confluenceblogtoindexfieldmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)