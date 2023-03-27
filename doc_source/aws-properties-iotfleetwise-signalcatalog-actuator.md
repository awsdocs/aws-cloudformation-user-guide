# AWS::IoTFleetWise::SignalCatalog Actuator<a name="aws-properties-iotfleetwise-signalcatalog-actuator"></a>

A signal that represents a vehicle device such as the engine, heater, and door locks\. Data from an actuator reports the state of a certain vehicle device\.

**Note**  
 Updating actuator data can change the state of a device\. For example, you can turn on or off the heater by updating its actuator data\.

## Syntax<a name="aws-properties-iotfleetwise-signalcatalog-actuator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-signalcatalog-actuator-syntax.json"></a>

```
{
  "[AllowedValues](#cfn-iotfleetwise-signalcatalog-actuator-allowedvalues)" : [ String, ... ],
  "[AssignedValue](#cfn-iotfleetwise-signalcatalog-actuator-assignedvalue)" : String,
  "[DataType](#cfn-iotfleetwise-signalcatalog-actuator-datatype)" : String,
  "[Description](#cfn-iotfleetwise-signalcatalog-actuator-description)" : String,
  "[FullyQualifiedName](#cfn-iotfleetwise-signalcatalog-actuator-fullyqualifiedname)" : String,
  "[Max](#cfn-iotfleetwise-signalcatalog-actuator-max)" : Double,
  "[Min](#cfn-iotfleetwise-signalcatalog-actuator-min)" : Double,
  "[Unit](#cfn-iotfleetwise-signalcatalog-actuator-unit)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-signalcatalog-actuator-syntax.yaml"></a>

```
  [AllowedValues](#cfn-iotfleetwise-signalcatalog-actuator-allowedvalues): 
    - String
  [AssignedValue](#cfn-iotfleetwise-signalcatalog-actuator-assignedvalue): String
  [DataType](#cfn-iotfleetwise-signalcatalog-actuator-datatype): String
  [Description](#cfn-iotfleetwise-signalcatalog-actuator-description): String
  [FullyQualifiedName](#cfn-iotfleetwise-signalcatalog-actuator-fullyqualifiedname): String
  [Max](#cfn-iotfleetwise-signalcatalog-actuator-max): Double
  [Min](#cfn-iotfleetwise-signalcatalog-actuator-min): Double
  [Unit](#cfn-iotfleetwise-signalcatalog-actuator-unit): String
```

## Properties<a name="aws-properties-iotfleetwise-signalcatalog-actuator-properties"></a>

`AllowedValues`  <a name="cfn-iotfleetwise-signalcatalog-actuator-allowedvalues"></a>
A list of possible values an actuator can take\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssignedValue`  <a name="cfn-iotfleetwise-signalcatalog-actuator-assignedvalue"></a>
A specified value for the actuator\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataType`  <a name="cfn-iotfleetwise-signalcatalog-actuator-datatype"></a>
The specified data type of the actuator\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `BOOLEAN | BOOLEAN_ARRAY | DOUBLE | DOUBLE_ARRAY | FLOAT | FLOAT_ARRAY | INT16 | INT16_ARRAY | INT32 | INT32_ARRAY | INT64 | INT64_ARRAY | INT8 | INT8_ARRAY | STRING | STRING_ARRAY | UINT16 | UINT16_ARRAY | UINT32 | UINT32_ARRAY | UINT64 | UINT64_ARRAY | UINT8 | UINT8_ARRAY | UNIX_TIMESTAMP | UNIX_TIMESTAMP_ARRAY | UNKNOWN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iotfleetwise-signalcatalog-actuator-description"></a>
A brief description of the actuator\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[^\u0000-\u001F\u007F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FullyQualifiedName`  <a name="cfn-iotfleetwise-signalcatalog-actuator-fullyqualifiedname"></a>
The fully qualified name of the actuator\. For example, the fully qualified name of an actuator might be `Vehicle.Front.Left.Door.Lock`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Max`  <a name="cfn-iotfleetwise-signalcatalog-actuator-max"></a>
The specified possible maximum value of an actuator\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-iotfleetwise-signalcatalog-actuator-min"></a>
The specified possible minimum value of an actuator\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-iotfleetwise-signalcatalog-actuator-unit"></a>
The scientific unit for the actuator\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)