# AWS::IoTEvents::DetectorModel AssetPropertyTimestamp<a name="aws-properties-iotevents-detectormodel-assetpropertytimestamp"></a>

A structure that contains timestamp information\. For more information, see [TimeInNanos](https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_TimeInNanos.html) in the *AWS IoT SiteWise API Reference*\.

For parameters that are string data type, you can specify the following options:
+ Use a string\. For example, the `timeInSeconds` value can be `'1586400675'`\.
+ Use an expression\. For example, the `timeInSeconds` value can be `'${$input.TemperatureInput.sensorData.timestamp/1000}'`\.

  For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the *AWS IoT Events Developer Guide*\.

## Syntax<a name="aws-properties-iotevents-detectormodel-assetpropertytimestamp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-assetpropertytimestamp-syntax.json"></a>

```
{
  "[OffsetInNanos](#cfn-iotevents-detectormodel-assetpropertytimestamp-offsetinnanos)" : String,
  "[TimeInSeconds](#cfn-iotevents-detectormodel-assetpropertytimestamp-timeinseconds)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-assetpropertytimestamp-syntax.yaml"></a>

```
  [OffsetInNanos](#cfn-iotevents-detectormodel-assetpropertytimestamp-offsetinnanos): String
  [TimeInSeconds](#cfn-iotevents-detectormodel-assetpropertytimestamp-timeinseconds): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-assetpropertytimestamp-properties"></a>

`OffsetInNanos`  <a name="cfn-iotevents-detectormodel-assetpropertytimestamp-offsetinnanos"></a>
The nanosecond offset converted from `timeInSeconds`\. The valid range is between 0\-999999999\. You can also specify an expression\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeInSeconds`  <a name="cfn-iotevents-detectormodel-assetpropertytimestamp-timeinseconds"></a>
The timestamp, in seconds, in the Unix epoch format\. The valid range is between 1\-31556889864403199\. You can also specify an expression\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)