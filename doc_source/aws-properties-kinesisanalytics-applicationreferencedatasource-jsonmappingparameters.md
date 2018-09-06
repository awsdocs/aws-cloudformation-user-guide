# Amazon Kinesis Data Analytics ApplicationReferenceDataSource JSONMappingParameters<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters"></a>

Provides additional mapping information when JSON is the record format on the streaming source\.

 `JSONMappingParameters` is a property of the [Kinesis Data Analytics ApplicationReferenceDataSource MappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters.md) parameter\. 

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-syntax.json"></a>

```
{
  "[RecordRowPath](#cfn-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-recordrowpath)" : String
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-syntax.yaml"></a>

```
  [RecordRowPath](#cfn-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-recordrowpath): String
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-properties"></a>

`RecordRowPath`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters-recordrowpath"></a>
Path to the top\-level parent that contains the records \(e\.g\., "$"\.\)  
 *Required*: Yes  
 *Type*: String;  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 