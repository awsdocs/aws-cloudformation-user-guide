# AWS::IoTEvents::DetectorModel SetTimer<a name="aws-properties-iotevents-detectormodel-settimer"></a>

Information needed to set the timer\.

## Syntax<a name="aws-properties-iotevents-detectormodel-settimer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-settimer-syntax.json"></a>

```
{
  "[Seconds](#cfn-iotevents-detectormodel-settimer-seconds)" : Integer,
  "[TimerName](#cfn-iotevents-detectormodel-settimer-timername)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-settimer-syntax.yaml"></a>

```
  [Seconds](#cfn-iotevents-detectormodel-settimer-seconds): Integer
  [TimerName](#cfn-iotevents-detectormodel-settimer-timername): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-settimer-properties"></a>

`Seconds`  <a name="cfn-iotevents-detectormodel-settimer-seconds"></a>
The number of seconds until the timer expires\. The minimum value is 60 seconds to ensure accuracy\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimerName`  <a name="cfn-iotevents-detectormodel-settimer-timername"></a>
The name of the timer\.  
*Required*: No  
*Type*: String  
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
