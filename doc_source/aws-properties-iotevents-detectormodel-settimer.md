# AWS::IoTEvents::DetectorModel SetTimer<a name="aws-properties-iotevents-detectormodel-settimer"></a>

Information needed to set the timer\.

## Syntax<a name="aws-properties-iotevents-detectormodel-settimer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotevents-detectormodel-settimer-syntax.json"></a>

```
{
  "[DurationExpression](#cfn-iotevents-detectormodel-settimer-durationexpression)" : String,
  "[Seconds](#cfn-iotevents-detectormodel-settimer-seconds)" : Integer,
  "[TimerName](#cfn-iotevents-detectormodel-settimer-timername)" : String
}
```

### YAML<a name="aws-properties-iotevents-detectormodel-settimer-syntax.yaml"></a>

```
  [DurationExpression](#cfn-iotevents-detectormodel-settimer-durationexpression): String
  [Seconds](#cfn-iotevents-detectormodel-settimer-seconds): Integer
  [TimerName](#cfn-iotevents-detectormodel-settimer-timername): String
```

## Properties<a name="aws-properties-iotevents-detectormodel-settimer-properties"></a>

`DurationExpression`  <a name="cfn-iotevents-detectormodel-settimer-durationexpression"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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