# AWS::IoTFleetWise::SignalCatalog Sensor<a name="aws-properties-iotfleetwise-signalcatalog-sensor"></a>

An input component that reports the environmental condition of a vehicle\.

**Note**  
You can collect data about fluid levels, temperatures, vibrations, or battery voltage from sensors\.

## Syntax<a name="aws-properties-iotfleetwise-signalcatalog-sensor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-signalcatalog-sensor-syntax.json"></a>

```
{
  "[AllowedValues](#cfn-iotfleetwise-signalcatalog-sensor-allowedvalues)" : [ String, ... ],
  "[DataType](#cfn-iotfleetwise-signalcatalog-sensor-datatype)" : String,
  "[Description](#cfn-iotfleetwise-signalcatalog-sensor-description)" : String,
  "[FullyQualifiedName](#cfn-iotfleetwise-signalcatalog-sensor-fullyqualifiedname)" : String,
  "[Max](#cfn-iotfleetwise-signalcatalog-sensor-max)" : Double,
  "[Min](#cfn-iotfleetwise-signalcatalog-sensor-min)" : Double,
  "[Unit](#cfn-iotfleetwise-signalcatalog-sensor-unit)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-signalcatalog-sensor-syntax.yaml"></a>

```
  [AllowedValues](#cfn-iotfleetwise-signalcatalog-sensor-allowedvalues): 
    - String
  [DataType](#cfn-iotfleetwise-signalcatalog-sensor-datatype): String
  [Description](#cfn-iotfleetwise-signalcatalog-sensor-description): String
  [FullyQualifiedName](#cfn-iotfleetwise-signalcatalog-sensor-fullyqualifiedname): String
  [Max](#cfn-iotfleetwise-signalcatalog-sensor-max): Double
  [Min](#cfn-iotfleetwise-signalcatalog-sensor-min): Double
  [Unit](#cfn-iotfleetwise-signalcatalog-sensor-unit): String
```

## Properties<a name="aws-properties-iotfleetwise-signalcatalog-sensor-properties"></a>

`AllowedValues`  <a name="cfn-iotfleetwise-signalcatalog-sensor-allowedvalues"></a>
A list of possible values a sensor can take\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataType`  <a name="cfn-iotfleetwise-signalcatalog-sensor-datatype"></a>
The specified data type of the sensor\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `BOOLEAN | BOOLEAN_ARRAY | DOUBLE | DOUBLE_ARRAY | FLOAT | FLOAT_ARRAY | INT16 | INT16_ARRAY | INT32 | INT32_ARRAY | INT64 | INT64_ARRAY | INT8 | INT8_ARRAY | STRING | STRING_ARRAY | UINT16 | UINT16_ARRAY | UINT32 | UINT32_ARRAY | UINT64 | UINT64_ARRAY | UINT8 | UINT8_ARRAY | UNIX_TIMESTAMP | UNIX_TIMESTAMP_ARRAY | UNKNOWN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iotfleetwise-signalcatalog-sensor-description"></a>
A brief description of a sensor\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[^\u0000-\u001F\u007F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FullyQualifiedName`  <a name="cfn-iotfleetwise-signalcatalog-sensor-fullyqualifiedname"></a>
The fully qualified name of the sensor\. For example, the fully qualified name of a sensor might be `Vehicle.Body.Engine.Battery`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Max`  <a name="cfn-iotfleetwise-signalcatalog-sensor-max"></a>
The specified possible maximum value of the sensor\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-iotfleetwise-signalcatalog-sensor-min"></a>
The specified possible minimum value of the sensor\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-iotfleetwise-signalcatalog-sensor-unit"></a>
The scientific unit of measurement for data collected by the sensor\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)