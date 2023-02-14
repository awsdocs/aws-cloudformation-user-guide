# AWS::IoT::FleetMetric AggregationType<a name="aws-properties-iot-fleetmetric-aggregationtype"></a>

The type of aggregation queries\.

## Syntax<a name="aws-properties-iot-fleetmetric-aggregationtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-fleetmetric-aggregationtype-syntax.json"></a>

```
{
  "[Name](#cfn-iot-fleetmetric-aggregationtype-name)" : String,
  "[Values](#cfn-iot-fleetmetric-aggregationtype-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-iot-fleetmetric-aggregationtype-syntax.yaml"></a>

```
  [Name](#cfn-iot-fleetmetric-aggregationtype-name): String
  [Values](#cfn-iot-fleetmetric-aggregationtype-values): 
    - String
```

## Properties<a name="aws-properties-iot-fleetmetric-aggregationtype-properties"></a>

`Name`  <a name="cfn-iot-fleetmetric-aggregationtype-name"></a>
The name of the aggregation type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-iot-fleetmetric-aggregationtype-values"></a>
A list of the values of aggregation types\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)