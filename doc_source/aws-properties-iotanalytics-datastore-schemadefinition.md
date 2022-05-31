# AWS::IoTAnalytics::Datastore SchemaDefinition<a name="aws-properties-iotanalytics-datastore-schemadefinition"></a>

Information needed to define a schema\.

## Syntax<a name="aws-properties-iotanalytics-datastore-schemadefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-schemadefinition-syntax.json"></a>

```
{
  "[Columns](#cfn-iotanalytics-datastore-schemadefinition-columns)" : [ Column, ... ]
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-schemadefinition-syntax.yaml"></a>

```
  [Columns](#cfn-iotanalytics-datastore-schemadefinition-columns): 
    - Column
```

## Properties<a name="aws-properties-iotanalytics-datastore-schemadefinition-properties"></a>

`Columns`  <a name="cfn-iotanalytics-datastore-schemadefinition-columns"></a>
Specifies one or more columns that store your data\.  
Each schema can have up to 100 columns\. Each column can have up to 100 nested types\.  
*Required*: No  
*Type*: List of [Column](aws-properties-iotanalytics-datastore-column.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)