# AWS::IoTAnalytics::Datastore FileFormatConfiguration<a name="aws-properties-iotanalytics-datastore-fileformatconfiguration"></a>

Contains the configuration information of file formats\. AWS IoT Analytics data stores support JSON and [Parquet](https://parquet.apache.org/)\.

The default file format is JSON\. You can specify only one format\.

You can't change the file format after you create the data store\.

## Syntax<a name="aws-properties-iotanalytics-datastore-fileformatconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-fileformatconfiguration-syntax.json"></a>

```
{
  "[JsonConfiguration](#cfn-iotanalytics-datastore-fileformatconfiguration-jsonconfiguration)" : Json,
  "[ParquetConfiguration](#cfn-iotanalytics-datastore-fileformatconfiguration-parquetconfiguration)" : ParquetConfiguration
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-fileformatconfiguration-syntax.yaml"></a>

```
  [JsonConfiguration](#cfn-iotanalytics-datastore-fileformatconfiguration-jsonconfiguration): 
    Json
  [ParquetConfiguration](#cfn-iotanalytics-datastore-fileformatconfiguration-parquetconfiguration): 
    ParquetConfiguration
```

## Properties<a name="aws-properties-iotanalytics-datastore-fileformatconfiguration-properties"></a>

`JsonConfiguration`  <a name="cfn-iotanalytics-datastore-fileformatconfiguration-jsonconfiguration"></a>
Contains the configuration information of the JSON format\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParquetConfiguration`  <a name="cfn-iotanalytics-datastore-fileformatconfiguration-parquetconfiguration"></a>
Contains the configuration information of the Parquet format\.  
*Required*: No  
*Type*: [ParquetConfiguration](aws-properties-iotanalytics-datastore-parquetconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)