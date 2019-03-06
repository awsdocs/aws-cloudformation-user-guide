# Amazon Kinesis Data Analytics Application JSONMappingParameters<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters"></a>

<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-description"></a>The `JSONMappingParameters` property type specifies additional mapping information for a SQL\-based Kinesis Data Analytics application when JSON is the record format on the streaming source\.

<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-inheritance"></a> `JSONMappingParameters` is a property of the [MappingParameters](aws-properties-kinesisanalyticsv2-application-mappingparameters.md) property\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-syntax.json"></a>

```
{
  "[RecordRowPath](#cfn-kinesisanalyticsv2-application-jsonmappingparameters-recordrowpath)" : String
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-syntax.yaml"></a>

```
[RecordRowPath](#cfn-kinesisanalyticsv2-application-jsonmappingparameters-recordrowpath): String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-jsonmappingparameters-properties"></a>

`RecordRowPath`  <a name="cfn-kinesisanalyticsv2-application-jsonmappingparameters-recordrowpath"></a>
The path to the top\-level parent that contains the records\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 