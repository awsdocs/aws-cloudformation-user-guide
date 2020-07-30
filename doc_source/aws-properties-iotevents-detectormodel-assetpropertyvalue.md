# AWS::IoTEvents::DetectorModel AssetPropertyValue<a name="aws-properties-iotevents-detectormodel-assetpropertyvalue"></a>

A structure that contains value information\. For more information, see [AssetPropertyValue](https://docs.aws.amazon.com/iot-sitewise/latest/APIReference/API_AssetPropertyValue.html) in the *AWS IoT SiteWise API Reference*\.

You must use expressions for all parameters in `AssetPropertyValue`\. The expressions accept literals, operators, functions, references, and substitution templates\.

**Examples**
+ For literal values, the expressions must contain single quotes\. For example, the value for the `quality` parameter can be `'GOOD'`\.
+ For references, you must specify either variables or input values\. For example, the value for the `quality` parameter can be `$input.TemperatureInput.sensorData.quality`\.

For more information, see [Syntax](https://docs.aws.amazon.com/iotevents/latest/developerguide/expression-syntax.html) in the *AWS IoT Events Developer Guide*\.

## Syntax<a name="aws-properties-iotevents-detectormodel-assetpropertyvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-assetpropertyvalue-syntax.json"></a>

```
{
  "[Quality](#cfn-iotevents-detectormodel-assetpropertyvalue-quality)" : String,
  "[Timestamp](#cfn-iotevents-detectormodel-assetpropertyvalue-timestamp)" : AssetPropertyTimestamp,
  "[Value](#cfn-iotevents-detectormodel-assetpropertyvalue-value)" : AssetPropertyVariant
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-assetpropertyvalue-syntax.yaml"></a>

```
  [Quality](#cfn-iotevents-detectormodel-assetpropertyvalue-quality): String
  [Timestamp](#cfn-iotevents-detectormodel-assetpropertyvalue-timestamp): 
    AssetPropertyTimestamp
  [Value](#cfn-iotevents-detectormodel-assetpropertyvalue-value): 
    AssetPropertyVariant
```

## Properties<a name="aws-properties-iotevents-detectormodel-assetpropertyvalue-properties"></a>

`Quality`  <a name="cfn-iotevents-detectormodel-assetpropertyvalue-quality"></a>
The quality of the asset property value\. The value must be `'GOOD'`, `'BAD'`, or `'UNCERTAIN'`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timestamp`  <a name="cfn-iotevents-detectormodel-assetpropertyvalue-timestamp"></a>
The timestamp associated with the asset property value\. The default is the current event time\.  
*Required*: No  
*Type*: [AssetPropertyTimestamp](aws-properties-iotevents-detectormodel-assetpropertytimestamp.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iotevents-detectormodel-assetpropertyvalue-value"></a>
The value to send to an asset property\.  
*Required*: No  
*Type*: [AssetPropertyVariant](aws-properties-iotevents-detectormodel-assetpropertyvariant.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)