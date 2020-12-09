# AWS::GroundStation::Config TrackingConfig<a name="aws-properties-groundstation-config-trackingconfig"></a>

 Provides information about how AWS Ground Station should track the satellite through the sky during a contact\. 

## Syntax<a name="aws-properties-groundstation-config-trackingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-trackingconfig-syntax.json"></a>

```
{
  "[AutoTrack](#cfn-groundstation-config-trackingconfig-autotrack)" : String
}
```

### YAML<a name="aws-properties-groundstation-config-trackingconfig-syntax.yaml"></a>

```
  [AutoTrack](#cfn-groundstation-config-trackingconfig-autotrack): String
```

## Properties<a name="aws-properties-groundstation-config-trackingconfig-properties"></a>

`AutoTrack`  <a name="cfn-groundstation-config-trackingconfig-autotrack"></a>
 Specifies whether or not to use autotrack\. `REMOVED` specifies that program track should only be used during the contact\. `PREFERRED` specifies that autotracking is preferred during the contact but fallback to program track if the signal is lost\. `REQUIRED` specifies that autotracking is required during the contact and not to use program track if the signal is lost\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-trackingconfig--examples"></a>

### Create a TrackingConfig<a name="aws-properties-groundstation-config-trackingconfig--examples--Create_a_TrackingConfig"></a>

The following example creates a Ground Station `TrackingConfig`

#### JSON<a name="aws-properties-groundstation-config-trackingconfig--examples--Create_a_TrackingConfig--json"></a>

```
{
  "TrackingConfig": {
    "Autotrack": "PREFERRED"
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-trackingconfig--examples--Create_a_TrackingConfig--yaml"></a>

```
TrackingConfig:
  Autotrack: "PREFERRED"
```