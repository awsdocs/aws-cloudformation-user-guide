# AWS::KinesisAnalyticsV2::Application MappingParameters<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters"></a>

When you configure a SQL\-based Kinesis Data Analytics application's input at the time of creating or updating an application, provides additional mapping information specific to the record format \(such as JSON, CSV, or record fields delimited by some delimiter\) on the streaming source\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-syntax.json"></a>

```
{
  "[CSVMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-csvmappingparameters)" : CSVMappingParameters,
  "[JSONMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-jsonmappingparameters)" : JSONMappingParameters
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-syntax.yaml"></a>

```
  [CSVMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-csvmappingparameters): 
    CSVMappingParameters
  [JSONMappingParameters](#cfn-kinesisanalyticsv2-application-mappingparameters-jsonmappingparameters): 
    JSONMappingParameters
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters-properties"></a>

`CSVMappingParameters`  <a name="cfn-kinesisanalyticsv2-application-mappingparameters-csvmappingparameters"></a>
Provides additional mapping information when the record format uses delimiters \(for example, CSV\)\.  
*Required*: No  
*Type*: [CSVMappingParameters](aws-properties-kinesisanalyticsv2-application-csvmappingparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JSONMappingParameters`  <a name="cfn-kinesisanalyticsv2-application-mappingparameters-jsonmappingparameters"></a>
Provides additional mapping information when JSON is the record format on the streaming source\.  
*Required*: No  
*Type*: [JSONMappingParameters](aws-properties-kinesisanalyticsv2-application-jsonmappingparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-kinesisanalyticsv2-application-mappingparameters--seealso"></a>
+  [MappingParameters](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_MappingParameters.html) in the *Amazon Kinesis Data Analytics API Reference* 

