# AWS::Kendra::DataSource ConfluenceBlogConfiguration<a name="aws-properties-kendra-datasource-confluenceblogconfiguration"></a>

Specifies the blog settings for the Confluence data source\. Blogs are always indexed unless filtered from the index by the `ExclusionPatterns` or `InclusionPatterns` fields in the `ConfluenceConfiguration` type\.

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
Defines how blog metadata fields should be mapped to index fields\. Before you can map a field, you must first create an index field with a matching type using the console or the `UpdateIndex` operation\.  
If you specify the `BlogFieldMappings` parameter, you must specify at least one field mapping\.  
*Required*: No  
*Type*: List of [ConfluenceBlogToIndexFieldMapping](aws-properties-kendra-datasource-confluenceblogtoindexfieldmapping.md)  
*Maximum*: `9`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)