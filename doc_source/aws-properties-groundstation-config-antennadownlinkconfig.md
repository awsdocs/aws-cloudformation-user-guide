# AWS::GroundStation::Config AntennaDownlinkConfig<a name="aws-properties-groundstation-config-antennadownlinkconfig"></a>

 Provides information about how AWS Ground Station should configure an antenna for downlink during a contact\. Use an antenna downlink config in a mission profile to receive the downlink data in raw DigIF format\. 

## Syntax<a name="aws-properties-groundstation-config-antennadownlinkconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-antennadownlinkconfig-syntax.json"></a>

```
{
  "[SpectrumConfig](#cfn-groundstation-config-antennadownlinkconfig-spectrumconfig)" : SpectrumConfig
}
```

### YAML<a name="aws-properties-groundstation-config-antennadownlinkconfig-syntax.yaml"></a>

```
  [SpectrumConfig](#cfn-groundstation-config-antennadownlinkconfig-spectrumconfig): 
    SpectrumConfig
```

## Properties<a name="aws-properties-groundstation-config-antennadownlinkconfig-properties"></a>

`SpectrumConfig`  <a name="cfn-groundstation-config-antennadownlinkconfig-spectrumconfig"></a>
 Defines the spectrum configuration\.   
*Required*: Yes  
*Type*: [SpectrumConfig](aws-properties-groundstation-config-spectrumconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-antennadownlinkconfig--examples"></a>

### Create an AntennaDownlinkConfig<a name="aws-properties-groundstation-config-antennadownlinkconfig--examples--Create_an_AntennaDownlinkConfig"></a>

The following example creates a Ground Station `AntennaDownlinkConfig`

#### JSON<a name="aws-properties-groundstation-config-antennadownlinkconfig--examples--Create_an_AntennaDownlinkConfig--json"></a>

```
{
  "AntennaDownlinkConfig": {
    "SpectrumConfig": {
    "CenterFrequency": {
      "Value": 7812,
      "Units": "MHz"
    },
    "Bandwidth": {
      "Value": 30,
      "Units": "MHz"
    },
    "Polarization": "RIGHT_HAND"
    }
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-antennadownlinkconfig--examples--Create_an_AntennaDownlinkConfig--yaml"></a>

```
AntennaDownlinkConfig:
  SpectrumConfig:
    CenterFrequency:
      Value: 7812
      Units: MHz
    Bandwidth:
      Value: 30
      Units: MHz
    Polarization: RIGHT_HAND
```