# AWS::IoTAnalytics::Datastore Column<a name="aws-properties-iotanalytics-datastore-column"></a>

Contains information about a column that stores your data\.

## Syntax<a name="aws-properties-iotanalytics-datastore-column-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-column-syntax.json"></a>

```
{
  "[Name](#cfn-iotanalytics-datastore-column-name)" : String,
  "[Type](#cfn-iotanalytics-datastore-column-type)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-column-syntax.yaml"></a>

```
  [Name](#cfn-iotanalytics-datastore-column-name): String
  [Type](#cfn-iotanalytics-datastore-column-type): String
```

## Properties<a name="aws-properties-iotanalytics-datastore-column-properties"></a>

`Name`  <a name="cfn-iotanalytics-datastore-column-name"></a>
The name of the column\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotanalytics-datastore-column-type"></a>
The type of data\. For more information about the supported data types, see [Common data types](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-common.html) in the * AWS Glue Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)