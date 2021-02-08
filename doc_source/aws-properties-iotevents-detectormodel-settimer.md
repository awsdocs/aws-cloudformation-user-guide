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
The duration of the timer, in seconds\. You can use a string expression that includes numbers, variables \(`$variable.<variable-name>`\), and input values \(`$input.<input-name>.<path-to-datum>`\) as the duration\. The range of the duration is 1\-31622400 seconds\. To ensure accuracy, the minimum duration is 60 seconds\. The evaluated result of the duration is rounded down to the nearest whole number\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Seconds`  <a name="cfn-iotevents-detectormodel-settimer-seconds"></a>
The number of seconds until the timer expires\. The minimum value is 60 seconds to ensure accuracy\. The maximum value is 31622400 seconds\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `31622400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimerName`  <a name="cfn-iotevents-detectormodel-settimer-timername"></a>
The name of the timer\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)