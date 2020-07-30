# AWS::IoTEvents::DetectorModel TransitionEvent<a name="aws-properties-iotevents-detectormodel-transitionevent"></a>

Specifies the actions performed and the next state entered when a `condition` evaluates to TRUE\.

## Syntax<a name="aws-properties-iotevents-detectormodel-transitionevent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-transitionevent-syntax.json"></a>

```
{
  "[Actions](#cfn-iotevents-detectormodel-transitionevent-actions)" : [ Action, ... ],
  "[Condition](#cfn-iotevents-detectormodel-transitionevent-condition)" : String,
  "[EventName](#cfn-iotevents-detectormodel-transitionevent-eventname)" : String,
  "[NextState](#cfn-iotevents-detectormodel-transitionevent-nextstate)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-transitionevent-syntax.yaml"></a>

```
  [Actions](#cfn-iotevents-detectormodel-transitionevent-actions): 
    - Action
  [Condition](#cfn-iotevents-detectormodel-transitionevent-condition): String
  [EventName](#cfn-iotevents-detectormodel-transitionevent-eventname): String
  [NextState](#cfn-iotevents-detectormodel-transitionevent-nextstate): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-transitionevent-properties"></a>

`Actions`  <a name="cfn-iotevents-detectormodel-transitionevent-actions"></a>
The actions to be performed\.  
*Required*: No  
*Type*: List of [Action](aws-properties-iotevents-detectormodel-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Condition`  <a name="cfn-iotevents-detectormodel-transitionevent-condition"></a>
Required\. A Boolean expression that when TRUE causes the actions to be performed and the `nextState` to be entered\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventName`  <a name="cfn-iotevents-detectormodel-transitionevent-eventname"></a>
The name of the transition event\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextState`  <a name="cfn-iotevents-detectormodel-transitionevent-nextstate"></a>
The next state to enter\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)