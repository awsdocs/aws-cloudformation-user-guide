# Amazon Kinesis Data Analytics Application JSONMappingParameters<a name="aws-properties-kinesisanalytics-application-jsonmappingparameters"></a>

The `JSONMappingParameters` property type specifies additional mapping information when JSON is the record format on the streaming source\. 

 `JSONMappingParameters` is a property of the [Kinesis Data Analytics Application MappingParameters](aws-properties-kinesisanalytics-application-mappingparameters.md) property type\. 

## Syntax<a name="aws-properties-kinesisanalytics-application-jsonmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-application-jsonmappingparameters-syntax.json"></a>

```
{
  "[RecordRowPath](#cfn-kinesisanalytics-application-jsonmappingparameters-recordrowpath)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-application-jsonmappingparameters-syntax.yaml"></a>

```
  [RecordRowPath](#cfn-kinesisanalytics-application-jsonmappingparameters-recordrowpath): String
```

## Properties<a name="aws-properties-kinesisanalytics-application-jsonmappingparameters-properties"></a>

`RecordRowPath`  <a name="cfn-kinesisanalytics-application-jsonmappingparameters-recordrowpath"></a>
The path to the top\-level parent that contains the records \(e\.g\., "$"\.\)  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 