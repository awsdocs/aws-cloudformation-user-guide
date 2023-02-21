# AWS::Kendra::DataSource ConfluencePageConfiguration<a name="aws-properties-kendra-datasource-confluencepageconfiguration"></a>

Configuration of the page settings for the Confluence data source\.

## Syntax<a name="aws-properties-kendra-datasource-confluencepageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluencepageconfiguration-syntax.json"></a>

```
{
  "[PageFieldMappings](#cfn-kendra-datasource-confluencepageconfiguration-pagefieldmappings)" : [ ConfluencePageToIndexFieldMapping, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-confluencepageconfiguration-syntax.yaml"></a>

```
  [PageFieldMappings](#cfn-kendra-datasource-confluencepageconfiguration-pagefieldmappings): 
    - ConfluencePageToIndexFieldMapping
```

## Properties<a name="aws-properties-kendra-datasource-confluencepageconfiguration-properties"></a>

`PageFieldMappings`  <a name="cfn-kendra-datasource-confluencepageconfiguration-pagefieldmappings"></a>
Maps attributes or field names of Confluence pages to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to Confluence fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The Confluence data source field names must exist in your Confluence custom metadata\.  
If you specify the `PageFieldMappings` parameter, you must specify at least one field mapping\.  
*Required*: No  
*Type*: List of [ConfluencePageToIndexFieldMapping](aws-properties-kendra-datasource-confluencepagetoindexfieldmapping.md)  
*Maximum*: `12`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)