# AWS::KinesisAnalytics::ApplicationReferenceDataSource MappingParameters<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters"></a>

When configuring application input at the time of creating or updating an application, provides additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the streaming source\.

## Syntax<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-syntax.json"></a>

```
{
  "[CSVMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-csvmappingparameters)" : CSVMappingParameters,
  "[JSONMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-jsonmappingparameters)" : JSONMappingParameters
}
```

### YAML<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-syntax.yaml"></a>

```
  [CSVMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-csvmappingparameters): 
    CSVMappingParameters
  [JSONMappingParameters](#cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-jsonmappingparameters): 
    JSONMappingParameters
```

## Properties<a name="aws-properties-kinesisanalytics-applicationreferencedatasource-mappingparameters-properties"></a>

`CSVMappingParameters`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-csvmappingparameters"></a>
Provides additional mapping information when the record format uses delimiters \(for example, CSV\)\.  
*Required*: No  
*Type*: [CSVMappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-csvmappingparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JSONMappingParameters`  <a name="cfn-kinesisanalytics-applicationreferencedatasource-mappingparameters-jsonmappingparameters"></a>
Provides additional mapping information when JSON is the record format on the streaming source\.  
*Required*: No  
*Type*: [JSONMappingParameters](aws-properties-kinesisanalytics-applicationreferencedatasource-jsonmappingparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)