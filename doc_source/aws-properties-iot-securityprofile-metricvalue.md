# AWS::IoT::SecurityProfile MetricValue<a name="aws-properties-iot-securityprofile-metricvalue"></a>

The value to be compared with the `metric`\.

## Syntax<a name="aws-properties-iot-securityprofile-metricvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-securityprofile-metricvalue-syntax.json"></a>

```
{
  "[Cidrs](#cfn-iot-securityprofile-metricvalue-cidrs)" : [ String, ... ],
  "[Count](#cfn-iot-securityprofile-metricvalue-count)" : String,
  "[Number](#cfn-iot-securityprofile-metricvalue-number)" : Double,
  "[Numbers](#cfn-iot-securityprofile-metricvalue-numbers)" : [ Double, ... ],
  "[Ports](#cfn-iot-securityprofile-metricvalue-ports)" : [ Integer, ... ],
  "[Strings](#cfn-iot-securityprofile-metricvalue-strings)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-iot-securityprofile-metricvalue-syntax.yaml"></a>

```
  [Cidrs](#cfn-iot-securityprofile-metricvalue-cidrs): 
    - String
  [Count](#cfn-iot-securityprofile-metricvalue-count): String
  [Number](#cfn-iot-securityprofile-metricvalue-number): Double
  [Numbers](#cfn-iot-securityprofile-metricvalue-numbers): 
    - Double
  [Ports](#cfn-iot-securityprofile-metricvalue-ports): 
    - Integer
  [Strings](#cfn-iot-securityprofile-metricvalue-strings): 
    - String
```

## Properties<a name="aws-properties-iot-securityprofile-metricvalue-properties"></a>

`Cidrs`  <a name="cfn-iot-securityprofile-metricvalue-cidrs"></a>
If the `comparisonOperator` calls for a set of CIDRs, use this to specify that set to be compared with the `metric`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Count`  <a name="cfn-iot-securityprofile-metricvalue-count"></a>
If the `comparisonOperator` calls for a numeric value, use this to specify that numeric value to be compared with the `metric`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Number`  <a name="cfn-iot-securityprofile-metricvalue-number"></a>
The numeric values of a metric\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Numbers`  <a name="cfn-iot-securityprofile-metricvalue-numbers"></a>
The numeric value of a metric\.  
*Required*: No  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ports`  <a name="cfn-iot-securityprofile-metricvalue-ports"></a>
If the `comparisonOperator` calls for a set of ports, use this to specify that set to be compared with the `metric`\.  
*Required*: No  
*Type*: List of Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Strings`  <a name="cfn-iot-securityprofile-metricvalue-strings"></a>
The string values of a metric\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)