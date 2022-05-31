# AWS::Kendra::DataSource ConfluenceBlogConfiguration<a name="aws-properties-kendra-datasource-confluenceblogconfiguration"></a>

Configuration of blog settings for the Confluence data source\. Blogs are always indexed unless filtered from the index by the `ExclusionPatterns` or `InclusionPatterns` fields in the `ConfluenceConfiguration` object\.

## Syntax<a name="aws-properties-kendra-datasource-confluenceblogconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluenceblogconfiguration-syntax.json"></a>

```
{
  "[BlogFieldMappings](#cfn-kendra-datasource-confluenceblogconfiguration-blogfieldmappings)" : [ ConfluenceBlogToIndexFieldMapping, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-confluenceblogconfiguration-syntax.yaml"></a>

```
  [BlogFieldMappings](#cfn-kendra-datasource-confluenceblogconfiguration-blogfieldmappings): 
    - ConfluenceBlogToIndexFieldMapping
```

## Properties<a name="aws-properties-kendra-datasource-confluenceblogconfiguration-properties"></a>

`BlogFieldMappings`  <a name="cfn-kendra-datasource-confluenceblogconfiguration-blogfieldmappings"></a>
Maps attributes or field names of Confluence blogs to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to Confluence fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The Confluence data source field names must exist in your Confluence custom metadata\.  
If you specify the `BlogFieldMappings` parameter, you must specify at least one field mapping\.  
*Required*: No  
*Type*: List of [ConfluenceBlogToIndexFieldMapping](aws-properties-kendra-datasource-confluenceblogtoindexfieldmapping.md)  
*Maximum*: `9`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)