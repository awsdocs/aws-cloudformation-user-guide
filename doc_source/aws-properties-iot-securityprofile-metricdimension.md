# AWS::IoT::SecurityProfile MetricDimension<a name="aws-properties-iot-securityprofile-metricdimension"></a>

The dimension of the metric\.

## Syntax<a name="aws-properties-iot-securityprofile-metricdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-securityprofile-metricdimension-syntax.json"></a>

```
{
  "[DimensionName](#cfn-iot-securityprofile-metricdimension-dimensionname)" : String,
  "[Operator](#cfn-iot-securityprofile-metricdimension-operator)" : String
}
```

### YAML<a name="aws-properties-iot-securityprofile-metricdimension-syntax.yaml"></a>

```
  [DimensionName](#cfn-iot-securityprofile-metricdimension-dimensionname): String
  [Operator](#cfn-iot-securityprofile-metricdimension-operator): String
```

## Properties<a name="aws-properties-iot-securityprofile-metricdimension-properties"></a>

`DimensionName`  <a name="cfn-iot-securityprofile-metricdimension-dimensionname"></a>
The name of the dimension\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operator`  <a name="cfn-iot-securityprofile-metricdimension-operator"></a>
Operators are constructs that perform logical operations\. Valid values are `IN` and `NOT_IN`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)