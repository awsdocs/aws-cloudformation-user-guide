# AWS::IoTEvents::DetectorModel OnInput<a name="aws-properties-iotevents-detectormodel-oninput"></a>

When an input is received and the `"condition"` is TRUE, perform the specified `"actions"`\.

## Syntax<a name="aws-properties-iotevents-detectormodel-oninput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-oninput-syntax.json"></a>

```
{
  "[Events](#cfn-iotevents-detectormodel-oninput-events)" : [ [Event](aws-properties-iotevents-detectormodel-event.md), ... ],
  "[TransitionEvents](#cfn-iotevents-detectormodel-oninput-transitionevents)" : [ [TransitionEvent](aws-properties-iotevents-detectormodel-transitionevent.md), ... ]
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-oninput-syntax.yaml"></a>

```
  [Events](#cfn-iotevents-detectormodel-oninput-events): 
    - [Event](aws-properties-iotevents-detectormodel-event.md)
  [TransitionEvents](#cfn-iotevents-detectormodel-oninput-transitionevents): 
    - [TransitionEvent](aws-properties-iotevents-detectormodel-transitionevent.md)
```

## Properties<a name="aws-properties-iotevents-detectormodel-oninput-properties"></a>

`Events`  <a name="cfn-iotevents-detectormodel-oninput-events"></a>
Specifies the actions that are performed when an input is received and the `"condition"` is TRUE\.  
*Required*: No  
*Type*: List of [Event](aws-properties-iotevents-detectormodel-event.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitionEvents`  <a name="cfn-iotevents-detectormodel-oninput-transitionevents"></a>
Specifies the actions performed, and the next state entered, when an input is received and a `"condition"` evaluates to TRUE\.  
*Required*: No  
*Type*: List of [TransitionEvent](aws-properties-iotevents-detectormodel-transitionevent.md)  
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
