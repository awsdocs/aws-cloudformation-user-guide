# AWS::IoTEvents::DetectorModel OnExit<a name="aws-properties-iotevents-detectormodel-onexit"></a>

When exiting this state, perform these `actions` if the specified `condition` is `TRUE`\.

## Syntax<a name="aws-properties-iotevents-detectormodel-onexit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-onexit-syntax.json"></a>

```
{
  "[Events](#cfn-iotevents-detectormodel-onexit-events)" : [ Event, ... ]
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-onexit-syntax.yaml"></a>

```
  [Events](#cfn-iotevents-detectormodel-onexit-events): 
    - Event
```

## Properties<a name="aws-properties-iotevents-detectormodel-onexit-properties"></a>

`Events`  <a name="cfn-iotevents-detectormodel-onexit-events"></a>
Specifies the `actions` that are performed when the state is exited and the `condition` is `TRUE`\.  
*Required*: No  
*Type*: List of [Event](aws-properties-iotevents-detectormodel-event.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)