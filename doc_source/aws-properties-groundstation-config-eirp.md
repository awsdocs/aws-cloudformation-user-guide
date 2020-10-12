# AWS::GroundStation::Config Eirp<a name="aws-properties-groundstation-config-eirp"></a>

 Defines an equivalent isotropically radiated power \(EIRP\)\. 

## Syntax<a name="aws-properties-groundstation-config-eirp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-eirp-syntax.json"></a>

```
{
  "[Units](#cfn-groundstation-config-eirp-units)" : String,
  "[Value](#cfn-groundstation-config-eirp-value)" : Double
}
```

### YAML<a name="aws-properties-groundstation-config-eirp-syntax.yaml"></a>

```
  [Units](#cfn-groundstation-config-eirp-units): String
  [Value](#cfn-groundstation-config-eirp-value): Double
```

## Properties<a name="aws-properties-groundstation-config-eirp-properties"></a>

`Units`  <a name="cfn-groundstation-config-eirp-units"></a>
 The units of the EIRP\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-groundstation-config-eirp-value"></a>
 The value of the EIRP\. Valid values are between 20\.0 to 50\.0 dBW\.   
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-eirp--examples"></a>

### Create an EIRP<a name="aws-properties-groundstation-config-eirp--examples--Create_an_EIRP"></a>

The following example creates a Ground Station `EIRP`

#### JSON<a name="aws-properties-groundstation-config-eirp--examples--Create_an_EIRP--json"></a>

```
{
  "TargetEirp": {
    "Value": 20,
    "Units": "dBW"
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-eirp--examples--Create_an_EIRP--yaml"></a>

```
TargetEirp:
  Value: 20.0
  Units: dBW
```