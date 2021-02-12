# AWS::IoTAnalytics::Datastore ParquetConfiguration<a name="aws-properties-iotanalytics-datastore-parquetconfiguration"></a>

Contains the configuration information of the Parquet format\.

## Syntax<a name="aws-properties-iotanalytics-datastore-parquetconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-parquetconfiguration-syntax.json"></a>

```
{
  "[SchemaDefinition](#cfn-iotanalytics-datastore-parquetconfiguration-schemadefinition)" : SchemaDefinition
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-parquetconfiguration-syntax.yaml"></a>

```
  [SchemaDefinition](#cfn-iotanalytics-datastore-parquetconfiguration-schemadefinition): 
    SchemaDefinition
```

## Properties<a name="aws-properties-iotanalytics-datastore-parquetconfiguration-properties"></a>

`SchemaDefinition`  <a name="cfn-iotanalytics-datastore-parquetconfiguration-schemadefinition"></a>
Information needed to define a schema\.  
*Required*: No  
*Type*: [SchemaDefinition](aws-properties-iotanalytics-datastore-schemadefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)