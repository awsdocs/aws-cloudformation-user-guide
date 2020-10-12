# AWS::IoT::TopicRule AssetPropertyTimestamp<a name="aws-properties-iot-topicrule-assetpropertytimestamp"></a>

An asset property timestamp entry containing the following information\.

## Syntax<a name="aws-properties-iot-topicrule-assetpropertytimestamp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-assetpropertytimestamp-syntax.json"></a>

```
{
  "[OffsetInNanos](#cfn-iot-topicrule-assetpropertytimestamp-offsetinnanos)" : String,
  "[TimeInSeconds](#cfn-iot-topicrule-assetpropertytimestamp-timeinseconds)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-assetpropertytimestamp-syntax.yaml"></a>

```
  [OffsetInNanos](#cfn-iot-topicrule-assetpropertytimestamp-offsetinnanos): String
  [TimeInSeconds](#cfn-iot-topicrule-assetpropertytimestamp-timeinseconds): String
```

## Properties<a name="aws-properties-iot-topicrule-assetpropertytimestamp-properties"></a>

`OffsetInNanos`  <a name="cfn-iot-topicrule-assetpropertytimestamp-offsetinnanos"></a>
Optional\. A string that contains the nanosecond time offset\. Accepts substitution templates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeInSeconds`  <a name="cfn-iot-topicrule-assetpropertytimestamp-timeinseconds"></a>
A string that contains the time in seconds since epoch\. Accepts substitution templates\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)