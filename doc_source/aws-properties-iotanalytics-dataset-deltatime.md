# AWS::IoTAnalytics::Dataset DeltaTime<a name="aws-properties-iotanalytics-dataset-deltatime"></a>

Used to limit data to that which has arrived since the last execution of the action\.

## Syntax<a name="aws-properties-iotanalytics-dataset-deltatime-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-deltatime-syntax.json"></a>

```
{
  "[OffsetSeconds](#cfn-iotanalytics-dataset-deltatime-offsetseconds)" : Integer,
  "[TimeExpression](#cfn-iotanalytics-dataset-deltatime-timeexpression)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-deltatime-syntax.yaml"></a>

```
﻿  [OffsetSeconds](#cfn-iotanalytics-dataset-deltatime-offsetseconds) : Integer
﻿  [TimeExpression](#cfn-iotanalytics-dataset-deltatime-timeexpression) : String
```

## Properties<a name="aws-properties-iotanalytics-dataset-deltatime-properties"></a>

`OffsetSeconds`  <a name="cfn-iotanalytics-dataset-deltatime-offsetseconds"></a>
The number of seconds of estimated "in flight" lag time of message data\. When you create data set contents using message data from a specified time frame, some message data may still be "in flight" when processing begins, and so will not arrive in time to be processed\. Use this field to make allowances for the "in flight" time of your message data, so that data not processed from a previous time frame will be included with the next time frame\. Without this, missed message data would be excluded from processing during the next time frame as well, because its timestamp places it within the previous time frame\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeExpression`  <a name="cfn-iotanalytics-dataset-deltatime-timeexpression"></a>
An expression by which the time of the message data may be determined\. This may be the name of a timestamp field, or a SQL expression which is used to derive the time the message data was generated\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)