# AWS::IoTEvents::DetectorModel AssetPropertyVariant<a name="aws-properties-iotevents-detectormodel-assetpropertyvariant"></a>

A structure that contains an asset property value\. For more information, see [Variant](https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_Variant.html) in the *AWS IoT SiteWise API Reference*\.

**Important**  
You must specify one of the following value types, depending on the `dataType` of the specified asset property\. For more information, see [AssetProperty](https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_AssetProperty.html) in the *AWS IoT SiteWise API Reference*\.

For parameters that are string data type, you can specify the following options:
+ Use a string\. For example, the `doubleValue` value can be `'47.9'`\.
+ Use an expression\. For example, the `doubleValue` value can be `$input.TemperatureInput.sensorData.temperature`\.

  For more information, see [Expressions](https://docs.aws.amazon.com/iotevents/latest/developerguide/iotevents-expressions.html) in the *AWS IoT Events Developer Guide*\.

## Syntax<a name="aws-properties-iotevents-detectormodel-assetpropertyvariant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-assetpropertyvariant-syntax.json"></a>

```
{
  "[BooleanValue](#cfn-iotevents-detectormodel-assetpropertyvariant-booleanvalue)" : String,
  "[DoubleValue](#cfn-iotevents-detectormodel-assetpropertyvariant-doublevalue)" : String,
  "[IntegerValue](#cfn-iotevents-detectormodel-assetpropertyvariant-integervalue)" : String,
  "[StringValue](#cfn-iotevents-detectormodel-assetpropertyvariant-stringvalue)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-assetpropertyvariant-syntax.yaml"></a>

```
  [BooleanValue](#cfn-iotevents-detectormodel-assetpropertyvariant-booleanvalue): String
  [DoubleValue](#cfn-iotevents-detectormodel-assetpropertyvariant-doublevalue): String
  [IntegerValue](#cfn-iotevents-detectormodel-assetpropertyvariant-integervalue): String
  [StringValue](#cfn-iotevents-detectormodel-assetpropertyvariant-stringvalue): 
    String
```

## Properties<a name="aws-properties-iotevents-detectormodel-assetpropertyvariant-properties"></a>

`BooleanValue`  <a name="cfn-iotevents-detectormodel-assetpropertyvariant-booleanvalue"></a>
The asset property value is a Boolean value that must be `TRUE` or `FALSE`\. You can also specify an expression\. If you use an expression, the evaluated result should be a Boolean value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DoubleValue`  <a name="cfn-iotevents-detectormodel-assetpropertyvariant-doublevalue"></a>
The asset property value is a double\. You can also specify an expression\. If you use an expression, the evaluated result should be a double\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerValue`  <a name="cfn-iotevents-detectormodel-assetpropertyvariant-integervalue"></a>
The asset property value is an integer\. You can also specify an expression\. If you use an expression, the evaluated result should be an integer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValue`  <a name="cfn-iotevents-detectormodel-assetpropertyvariant-stringvalue"></a>
The asset property value is a string\. You can also specify an expression\. If you use an expression, the evaluated result should be a string\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)