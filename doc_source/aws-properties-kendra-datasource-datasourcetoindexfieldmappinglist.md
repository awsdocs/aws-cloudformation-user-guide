# AWS::Kendra::DataSource DataSourceToIndexFieldMappingList<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist"></a>

Specifies a list of mappings that relate data source fields and attributes to index fields\.

## Syntax<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist-syntax.json"></a>

```
{
  "[DataSourceToIndexFieldMappingList](#cfn-kendra-datasource-datasourcetoindexfieldmappinglist-datasourcetoindexfieldmappinglist)" : [ DataSourceToIndexFieldMapping, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist-syntax.yaml"></a>

```
  [DataSourceToIndexFieldMappingList](#cfn-kendra-datasource-datasourcetoindexfieldmappinglist-datasourcetoindexfieldmappinglist): 
    - DataSourceToIndexFieldMapping
```

## Properties<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist-properties"></a>

`DataSourceToIndexFieldMappingList`  <a name="cfn-kendra-datasource-datasourcetoindexfieldmappinglist-datasourcetoindexfieldmappinglist"></a>
A list of `DataSourceToIndexFieldMapping` instances that relate data source fields and attributes to index fields\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist) of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)