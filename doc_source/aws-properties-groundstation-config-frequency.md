# AWS::GroundStation::Config Frequency<a name="aws-properties-groundstation-config-frequency"></a>

 Defines a frequency\. 

## Syntax<a name="aws-properties-groundstation-config-frequency-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-frequency-syntax.json"></a>

```
{
  "[Units](#cfn-groundstation-config-frequency-units)" : String,
  "[Value](#cfn-groundstation-config-frequency-value)" : Double
}
```

### YAML<a name="aws-properties-groundstation-config-frequency-syntax.yaml"></a>

```
  [Units](#cfn-groundstation-config-frequency-units): String
  [Value](#cfn-groundstation-config-frequency-value): Double
```

## Properties<a name="aws-properties-groundstation-config-frequency-properties"></a>

`Units`  <a name="cfn-groundstation-config-frequency-units"></a>
 The units of the frequency\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-groundstation-config-frequency-value"></a>
 The value of the frequency\. Valid values are between 2200 to 2300 MHz and 7750 to 8400 MHz for downlink and 2025 to 2120 MHz for uplink\.   
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-frequency--examples"></a>

### Create a Frequency<a name="aws-properties-groundstation-config-frequency--examples--Create_a_Frequency"></a>

The following example creates a Ground Station `Frequency`

#### JSON<a name="aws-properties-groundstation-config-frequency--examples--Create_a_Frequency--json"></a>

```
{
  "CenterFrequency": {
    "Value": 7812,
    "Units": "MHz"
  },
}
```

#### YAML<a name="aws-properties-groundstation-config-frequency--examples--Create_a_Frequency--yaml"></a>

```
CenterFrequency:
  Value: 7812
  Units: MHz
```