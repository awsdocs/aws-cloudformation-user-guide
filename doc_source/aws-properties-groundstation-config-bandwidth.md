# AWS::GroundStation::Config Bandwidth<a name="aws-properties-groundstation-config-bandwidth"></a>

 Defines a bandwidth\. 

## Syntax<a name="aws-properties-groundstation-config-bandwidth-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-bandwidth-syntax.json"></a>

```
{
  "[Units](#cfn-groundstation-config-frequency-units)" : String,
  "[Value](#cfn-groundstation-config-frequency-value)" : Double
}
```

### YAML<a name="aws-properties-groundstation-config-bandwidth-syntax.yaml"></a>

```
  [Units](#cfn-groundstation-config-frequency-units): String
  [Value](#cfn-groundstation-config-frequency-value): Double
```

## Properties<a name="aws-properties-groundstation-config-bandwidth-properties"></a>

`Units`  <a name="cfn-groundstation-config-frequency-units"></a>
 The units of the bandwidth\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-groundstation-config-frequency-value"></a>
 The value of the bandwidth\. AWS Ground Station currently has the following bandwidth limitations:   
+ For `AntennaDownlinkDemodDecodeconfig`, valid values are between 125 kHz to 650 MHz\.
+ For `AntennaDownlinkconfig`, valid values are between 10 kHz to 54 MHz\.
+ For `AntennaUplinkConfig`, valid values are between 10 kHz to 54 MHz\.
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-bandwidth--examples"></a>

### Create a Bandwidth<a name="aws-properties-groundstation-config-bandwidth--examples--Create_a_Bandwidth"></a>

The following example creates a Ground Station `Bandwidth`

#### JSON<a name="aws-properties-groundstation-config-bandwidth--examples--Create_a_Bandwidth--json"></a>

```
{
  "Bandwidth": {
    "Value": 30,
    "Units": "MHz"
  },
}
```

#### YAML<a name="aws-properties-groundstation-config-bandwidth--examples--Create_a_Bandwidth--yaml"></a>

```
Bandwidth:
  Value: 30
  Units: MHz
```