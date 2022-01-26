# AWS::IoT::TopicRule TimestreamAction<a name="aws-properties-iot-topicrule-timestreamaction"></a>

Describes an action that writes records into an Amazon Timestream table\.

## Syntax<a name="aws-properties-iot-topicrule-timestreamaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-timestreamaction-syntax.json"></a>

```
{
  "[BatchMode](#cfn-iot-topicrule-timestreamaction-batchmode)" : Boolean,
  "[DatabaseName](#cfn-iot-topicrule-timestreamaction-databasename)" : String,
  "[Dimensions](#cfn-iot-topicrule-timestreamaction-dimensions)" : [ TimestreamDimension, ... ],
  "[RoleArn](#cfn-iot-topicrule-timestreamaction-rolearn)" : String,
  "[TableName](#cfn-iot-topicrule-timestreamaction-tablename)" : String,
  "[Timestamp](#cfn-iot-topicrule-timestreamaction-timestamp)" : TimestreamTimestamp
}
```

### YAML<a name="aws-properties-iot-topicrule-timestreamaction-syntax.yaml"></a>

```
  [BatchMode](#cfn-iot-topicrule-timestreamaction-batchmode): Boolean
  [DatabaseName](#cfn-iot-topicrule-timestreamaction-databasename): String
  [Dimensions](#cfn-iot-topicrule-timestreamaction-dimensions): 
    - TimestreamDimension
  [RoleArn](#cfn-iot-topicrule-timestreamaction-rolearn): String
  [TableName](#cfn-iot-topicrule-timestreamaction-tablename): String
  [Timestamp](#cfn-iot-topicrule-timestreamaction-timestamp): 
    TimestreamTimestamp
```

## Properties<a name="aws-properties-iot-topicrule-timestreamaction-properties"></a>

`BatchMode`  <a name="cfn-iot-topicrule-timestreamaction-batchmode"></a>
Whether to process the action as a batch\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-iot-topicrule-timestreamaction-databasename"></a>
The name of an Amazon Timestream database that has the table to write records into\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dimensions`  <a name="cfn-iot-topicrule-timestreamaction-dimensions"></a>
Metadata attributes of the time series that are written in each measure record\.  
*Required*: Yes  
*Type*: List of [TimestreamDimension](aws-properties-iot-topicrule-timestreamdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-topicrule-timestreamaction-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that grants AWS IoT permission to write to the Timestream database table\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-iot-topicrule-timestreamaction-tablename"></a>
The table where the message data will be written\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timestamp`  <a name="cfn-iot-topicrule-timestreamaction-timestamp"></a>
The value to use for the entry's timestamp\. If blank, the time that the entry was processed is used\.  
*Required*: No  
*Type*: [TimestreamTimestamp](aws-properties-iot-topicrule-timestreamtimestamp.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)