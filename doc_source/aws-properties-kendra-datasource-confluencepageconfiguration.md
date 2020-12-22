# AWS::Kendra::DataSource ConfluencePageConfiguration<a name="aws-properties-kendra-datasource-confluencepageconfiguration"></a>

Specifies the page settings for the Confluence data source\.

## Syntax<a name="aws-properties-kendra-datasource-confluencepageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluencepageconfiguration-syntax.json"></a>

```
{
  "[PageFieldMappings](#cfn-kendra-datasource-confluencepageconfiguration-pagefieldmappings)" : ConfluencePageFieldMappingsList
}
```

### YAML<a name="aws-properties-kendra-datasource-confluencepageconfiguration-syntax.yaml"></a>

```
  [PageFieldMappings](#cfn-kendra-datasource-confluencepageconfiguration-pagefieldmappings): 
    ConfluencePageFieldMappingsList
```

## Properties<a name="aws-properties-kendra-datasource-confluencepageconfiguration-properties"></a>

`PageFieldMappings`  <a name="cfn-kendra-datasource-confluencepageconfiguration-pagefieldmappings"></a>
Defines how page metadata fields should be mapped to index fields\. Before you can map a field, you must first create an index field with a matching type using the console or the `UpdateIndex` operation\.  
If you specify the `PageFieldMappings` parameter, you must specify at least one field mapping\.  
*Required*: No  
*Type*: [ConfluencePageFieldMappingsList](aws-properties-kendra-datasource-confluencepagefieldmappingslist.md)  
*Maximum*: `12`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)