# AWS::IoT::TopicRule AssetPropertyVariant<a name="aws-properties-iot-topicrule-assetpropertyvariant"></a>

Contains an asset property value \(of a single type\)\.

## Syntax<a name="aws-properties-iot-topicrule-assetpropertyvariant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-assetpropertyvariant-syntax.json"></a>

```
{
  "[BooleanValue](#cfn-iot-topicrule-assetpropertyvariant-booleanvalue)" : String,
  "[DoubleValue](#cfn-iot-topicrule-assetpropertyvariant-doublevalue)" : String,
  "[IntegerValue](#cfn-iot-topicrule-assetpropertyvariant-integervalue)" : String,
  "[StringValue](#cfn-iot-topicrule-assetpropertyvariant-stringvalue)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-assetpropertyvariant-syntax.yaml"></a>

```
  [BooleanValue](#cfn-iot-topicrule-assetpropertyvariant-booleanvalue): String
  [DoubleValue](#cfn-iot-topicrule-assetpropertyvariant-doublevalue): String
  [IntegerValue](#cfn-iot-topicrule-assetpropertyvariant-integervalue): String
  [StringValue](#cfn-iot-topicrule-assetpropertyvariant-stringvalue): 
    String
```

## Properties<a name="aws-properties-iot-topicrule-assetpropertyvariant-properties"></a>

`BooleanValue`  <a name="cfn-iot-topicrule-assetpropertyvariant-booleanvalue"></a>
Optional\. A string that contains the boolean value \(`true` or `false`\) of the value entry\. Accepts substitution templates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DoubleValue`  <a name="cfn-iot-topicrule-assetpropertyvariant-doublevalue"></a>
Optional\. A string that contains the double value of the value entry\. Accepts substitution templates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerValue`  <a name="cfn-iot-topicrule-assetpropertyvariant-integervalue"></a>
Optional\. A string that contains the integer value of the value entry\. Accepts substitution templates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringValue`  <a name="cfn-iot-topicrule-assetpropertyvariant-stringvalue"></a>
Optional\. The string value of the value entry\. Accepts substitution templates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)