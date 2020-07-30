# AWS::GroundStation::Config AntennaUplinkConfig<a name="aws-properties-groundstation-config-antennauplinkconfig"></a>

 Provides information about how AWS Ground Station should configure an antenna for uplink during a contact\. 

## Syntax<a name="aws-properties-groundstation-config-antennauplinkconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-antennauplinkconfig-syntax.json"></a>

```
{
  "[SpectrumConfig](#cfn-groundstation-config-antennauplinkconfig-spectrumconfig)" : SpectrumConfig,
  "[TargetEirp](#cfn-groundstation-config-antennauplinkconfig-targeteirp)" : Eirp
}
```

### YAML<a name="aws-properties-groundstation-config-antennauplinkconfig-syntax.yaml"></a>

```
  [SpectrumConfig](#cfn-groundstation-config-antennauplinkconfig-spectrumconfig): 
    SpectrumConfig
  [TargetEirp](#cfn-groundstation-config-antennauplinkconfig-targeteirp): 
    Eirp
```

## Properties<a name="aws-properties-groundstation-config-antennauplinkconfig-properties"></a>

`SpectrumConfig`  <a name="cfn-groundstation-config-antennauplinkconfig-spectrumconfig"></a>
 Defines the spectrum configuration\.   
*Required*: Yes  
*Type*: [SpectrumConfig](aws-properties-groundstation-config-spectrumconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetEirp`  <a name="cfn-groundstation-config-antennauplinkconfig-targeteirp"></a>
 The equivalent isotropically radiated power \(EIRP\) to use for uplink transmissions\. Valid values are between 20\.0 to 50\.0 dBW\.   
*Required*: Yes  
*Type*: [Eirp](aws-properties-groundstation-config-eirp.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-antennauplinkconfig--examples"></a>

### Create an AntennaUplinkConfig<a name="aws-properties-groundstation-config-antennauplinkconfig--examples--Create_an_AntennaUplinkConfig"></a>

The following example creates a Ground Station `AntennaUplinkConfig`

#### JSON<a name="aws-properties-groundstation-config-antennauplinkconfig--examples--Create_an_AntennaUplinkConfig--json"></a>

```
{
  "AntennaUplinkConfig": {
    "SpectrumConfig": {
    "CenterFrequency": {
      "Value": 2072.5,
      "Units": "MHz"
    },
    "Polarization": "RIGHT_HAND"
    },
    "TargetEirp": {
      "Value": 20,
      "Units": "dBW"
    }
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-antennauplinkconfig--examples--Create_an_AntennaUplinkConfig--yaml"></a>

```
AntennaUplinkConfig:
  SpectrumConfig:
    CenterFrequency:
      Value: 2072.5
      Units: MHz
    Polarization: RIGHT_HAND
  TargetEirp:
    Value: 20.0
    Units: dBW
```