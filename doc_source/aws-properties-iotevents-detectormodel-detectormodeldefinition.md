# AWS::IoTEvents::DetectorModel DetectorModelDefinition<a name="aws-properties-iotevents-detectormodel-detectormodeldefinition"></a>

Information that defines how a detector operates\.

## Syntax<a name="aws-properties-iotevents-detectormodel-detectormodeldefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-detectormodeldefinition-syntax.json"></a>

```
{
  "[InitialStateName](#cfn-iotevents-detectormodel-detectormodeldefinition-initialstatename)" : String,
  "[States](#cfn-iotevents-detectormodel-detectormodeldefinition-states)" : [ [State](aws-properties-iotevents-detectormodel-state.md), ... ]
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-detectormodeldefinition-syntax.yaml"></a>

```
  [InitialStateName](#cfn-iotevents-detectormodel-detectormodeldefinition-initialstatename): String
  [States](#cfn-iotevents-detectormodel-detectormodeldefinition-states): 
    - [State](aws-properties-iotevents-detectormodel-state.md)
```

## Properties<a name="aws-properties-iotevents-detectormodel-detectormodeldefinition-properties"></a>

`InitialStateName`  <a name="cfn-iotevents-detectormodel-detectormodeldefinition-initialstatename"></a>
The state that is entered at the creation of each detector \(instance\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`States`  <a name="cfn-iotevents-detectormodel-detectormodeldefinition-states"></a>
Information about the states of the detector\.  
*Required*: No  
*Type*: List of [State](aws-properties-iotevents-detectormodel-state.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
