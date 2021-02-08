# AWS::IoTEvents::DetectorModel OnInput<a name="aws-properties-iotevents-detectormodel-oninput"></a>

Specifies the actions performed when the `condition` evaluates to TRUE\.

## Syntax<a name="aws-properties-iotevents-detectormodel-oninput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-oninput-syntax.json"></a>

```
{
  "[Events](#cfn-iotevents-detectormodel-oninput-events)" : [ Event, ... ],
  "[TransitionEvents](#cfn-iotevents-detectormodel-oninput-transitionevents)" : [ TransitionEvent, ... ]
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-oninput-syntax.yaml"></a>

```
  [Events](#cfn-iotevents-detectormodel-oninput-events): 
    - Event
  [TransitionEvents](#cfn-iotevents-detectormodel-oninput-transitionevents): 
    - TransitionEvent
```

## Properties<a name="aws-properties-iotevents-detectormodel-oninput-properties"></a>

`Events`  <a name="cfn-iotevents-detectormodel-oninput-events"></a>
Specifies the actions performed when the `condition` evaluates to TRUE\.  
*Required*: No  
*Type*: List of [Event](aws-properties-iotevents-detectormodel-event.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitionEvents`  <a name="cfn-iotevents-detectormodel-oninput-transitionevents"></a>
Specifies the actions performed, and the next state entered, when a `condition` evaluates to TRUE\.  
*Required*: No  
*Type*: List of [TransitionEvent](aws-properties-iotevents-detectormodel-transitionevent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)