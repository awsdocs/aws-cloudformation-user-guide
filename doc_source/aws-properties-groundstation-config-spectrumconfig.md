# AWS::GroundStation::Config SpectrumConfig<a name="aws-properties-groundstation-config-spectrumconfig"></a>

 Defines a spectrum\. 

## Syntax<a name="aws-properties-groundstation-config-spectrumconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-spectrumconfig-syntax.json"></a>

```
{
  "[Bandwidth](#cfn-groundstation-config-spectrumconfig-bandwidth)" : [Bandwidth](aws-properties-groundstation-config-bandwidth.md),
  "[CenterFrequency](#cfn-groundstation-config-spectrumconfig-centerfrequency)" : [Frequency](aws-properties-groundstation-config-frequency.md),
  "[Polarization](#cfn-groundstation-config-spectrumconfig-polarization)" : String
}
```

### YAML<a name="aws-properties-groundstation-config-spectrumconfig-syntax.yaml"></a>

```
  [Bandwidth](#cfn-groundstation-config-spectrumconfig-bandwidth): 
    [Bandwidth](aws-properties-groundstation-config-bandwidth.md)
  [CenterFrequency](#cfn-groundstation-config-spectrumconfig-centerfrequency): 
    [Frequency](aws-properties-groundstation-config-frequency.md)
  [Polarization](#cfn-groundstation-config-spectrumconfig-polarization): String
```

## Properties<a name="aws-properties-groundstation-config-spectrumconfig-properties"></a>

`Bandwidth`  <a name="cfn-groundstation-config-spectrumconfig-bandwidth"></a>
 The bandwidth of the spectrum\.   
*Required*: Yes  
*Type*: [Bandwidth](aws-properties-groundstation-config-bandwidth.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CenterFrequency`  <a name="cfn-groundstation-config-spectrumconfig-centerfrequency"></a>
 The center frequency of the spectrum\.   
*Required*: Yes  
*Type*: [Frequency](aws-properties-groundstation-config-frequency.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Polarization`  <a name="cfn-groundstation-config-spectrumconfig-polarization"></a>
 The polarization of the spectrum\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-spectrumconfig--examples"></a>

### Create a SpectrumConfig<a name="aws-properties-groundstation-config-spectrumconfig--examples--Create_a_SpectrumConfig"></a>

The following example creates a Ground Station `SpectrumConfig`

#### JSON<a name="aws-properties-groundstation-config-spectrumconfig--examples--Create_a_SpectrumConfig--json"></a>

```
{
  "SpectrumConfig": {
    "Bandwidth": {
      "Value": 30,
      "Units": "MHz"
    },
    "CenterFrequency": {
      "Value": 7812,
      "Units": "MHz"
    },
    "Polarization": "RIGHT_HAND"
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-spectrumconfig--examples--Create_a_SpectrumConfig--yaml"></a>

```
SpectrumConfig:
  Bandwidth:
    Value: 30
    Units: MHz
  CenterFrequency:
    Value: 7812
    Units: MHz
  Polarization: RIGHT_HAND
```