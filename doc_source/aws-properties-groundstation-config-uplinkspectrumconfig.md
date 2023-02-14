# AWS::GroundStation::Config UplinkSpectrumConfig<a name="aws-properties-groundstation-config-uplinkspectrumconfig"></a>

 Defines a uplink spectrum\. 

## Syntax<a name="aws-properties-groundstation-config-uplinkspectrumconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-uplinkspectrumconfig-syntax.json"></a>

```
{
  "[CenterFrequency](#cfn-groundstation-config-uplinkspectrumconfig-centerfrequency)" : Frequency,
  "[Polarization](#cfn-groundstation-config-uplinkspectrumconfig-polarization)" : String
}
```

### YAML<a name="aws-properties-groundstation-config-uplinkspectrumconfig-syntax.yaml"></a>

```
  [CenterFrequency](#cfn-groundstation-config-uplinkspectrumconfig-centerfrequency): 
    Frequency
  [Polarization](#cfn-groundstation-config-uplinkspectrumconfig-polarization): String
```

## Properties<a name="aws-properties-groundstation-config-uplinkspectrumconfig-properties"></a>

`CenterFrequency`  <a name="cfn-groundstation-config-uplinkspectrumconfig-centerfrequency"></a>
 The center frequency of the spectrum\. Valid values are between 2200 to 2300 MHz and 7750 to 8400 MHz for downlink and 2025 to 2120 MHz for uplink\.   
*Required*: No  
*Type*: [Frequency](aws-properties-groundstation-config-frequency.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Polarization`  <a name="cfn-groundstation-config-uplinkspectrumconfig-polarization"></a>
 The polarization of the spectrum\. Valid values are `"RIGHT_HAND"` and `"LEFT_HAND"`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-uplinkspectrumconfig--examples"></a>

### Create an uplink SpectrumConfig<a name="aws-properties-groundstation-config-uplinkspectrumconfig--examples--Create_an_uplink_SpectrumConfig"></a>

The following example creates a Ground Station `SpectrumConfig` for an uplink config

#### JSON<a name="aws-properties-groundstation-config-uplinkspectrumconfig--examples--Create_an_uplink_SpectrumConfig--json"></a>

```
{
  "SpectrumConfig": {
    
    "CenterFrequency": {
      "Value": 2100,
      "Units": "MHz"
    },
    "Polarization": "RIGHT_HAND"
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-uplinkspectrumconfig--examples--Create_an_uplink_SpectrumConfig--yaml"></a>

```
SpectrumConfig:
  CenterFrequency:
    Value: 2100
    Units: MHz
  Polarization: RIGHT_HAND
```