# AWS::IoTEvents::DetectorModel OnEnter<a name="aws-properties-iotevents-detectormodel-onenter"></a>

When entering this state, perform these `"actions"` if the `"condition"` is TRUE\.

## Syntax<a name="aws-properties-iotevents-detectormodel-onenter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-onenter-syntax.json"></a>

```
{
  "[Events](#cfn-iotevents-detectormodel-onenter-events)" : [ [Event](aws-properties-iotevents-detectormodel-event.md), ... ]
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-onenter-syntax.yaml"></a>

```
  [Events](#cfn-iotevents-detectormodel-onenter-events): 
    - [Event](aws-properties-iotevents-detectormodel-event.md)
```

## Properties<a name="aws-properties-iotevents-detectormodel-onenter-properties"></a>

`Events`  <a name="cfn-iotevents-detectormodel-onenter-events"></a>
Specifies the actions that are performed when the state is entered and the `"condition"` is TRUE\.  
*Required*: No  
*Type*: List of [Event](aws-properties-iotevents-detectormodel-event.md)  
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
