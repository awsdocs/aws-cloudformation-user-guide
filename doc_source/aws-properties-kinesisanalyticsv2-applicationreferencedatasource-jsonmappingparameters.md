# Amazon Kinesis Data Analytics ApplicationReferenceDataSource JSONMappingParameters<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters"></a>

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-description"></a>The `JSONMappingParameters` property type specifies additional mapping information when JSON is the record format on the reference source for a SQL\-based Amazon Kinesis Data Analytics application\.

<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-inheritance"></a> `JSONMappingParameters` is a property of the [MappingParameters](aws-properties-kinesisanalyticsv2-applicationreferencedatasource-mappingparameters.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-syntax.json"></a>

```
{
  "[RecordRowPath](#cfn-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-recordrowpath)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-syntax.yaml"></a>

```
[RecordRowPath](#cfn-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-recordrowpath): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-properties"></a>

`RecordRowPath`  <a name="cfn-kinesisanalyticsv2-applicationreferencedatasource-jsonmappingparameters-recordrowpath"></a>
The path to the top\-level parent that contains the records\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 