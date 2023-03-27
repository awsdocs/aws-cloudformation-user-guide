# AWS::IoTEvents::AlarmModel AssetPropertyTimestamp<a name="aws-properties-iotevents-alarmmodel-assetpropertytimestamp"></a>

A structure that contains timestamp information\. For more information, see [TimeInNanos](https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_TimeInNanos.html) in the * AWS IoT SiteWise API Reference*\.

You must use expressions for all parameters in `AssetPropertyTimestamp`\. The expressions accept literals, operators, functions, references, and substitution templates\.

**Examples**
+ For literal values, the expressions must contain single quotes\. For example, the value for the `timeInSeconds` parameter can be `'1586400675'`\.
+ For references, you must specify either variables or input values\. For example, the value for the `offsetInNanos` parameter can be `$variable.time`\.
+ For a substitution template, you must use `${}`, and the template must be in single quotes\. A substitution template can also contain a combination of literals, operators, functions, references, and substitution templates\.

  In the following example, the value for the `timeInSeconds` parameter uses a substitution template\.

   `'${$input.TemperatureInput.sensorData.timestamp / 1000}'` 

For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the * AWS IoT Events Developer Guide*\.

## Syntax<a name="aws-properties-iotevents-alarmmodel-assetpropertytimestamp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-alarmmodel-assetpropertytimestamp-syntax.json"></a>

```
{
  "[OffsetInNanos](#cfn-iotevents-alarmmodel-assetpropertytimestamp-offsetinnanos)" : String,
  "[TimeInSeconds](#cfn-iotevents-alarmmodel-assetpropertytimestamp-timeinseconds)" : String
}
```

### YAML<a name="aws-properties-iotevents-alarmmodel-assetpropertytimestamp-syntax.yaml"></a>

```
  [OffsetInNanos](#cfn-iotevents-alarmmodel-assetpropertytimestamp-offsetinnanos): String
  [TimeInSeconds](#cfn-iotevents-alarmmodel-assetpropertytimestamp-timeinseconds): String
```

## Properties<a name="aws-properties-iotevents-alarmmodel-assetpropertytimestamp-properties"></a>

`OffsetInNanos`  <a name="cfn-iotevents-alarmmodel-assetpropertytimestamp-offsetinnanos"></a>
The nanosecond offset converted from `timeInSeconds`\. The valid range is between 0\-999999999\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeInSeconds`  <a name="cfn-iotevents-alarmmodel-assetpropertytimestamp-timeinseconds"></a>
The timestamp, in seconds, in the Unix epoch format\. The valid range is between 1\-31556889864403199\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)