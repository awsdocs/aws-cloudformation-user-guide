# AWS::IoTFleetWise::Campaign SignalInformation<a name="aws-properties-iotfleetwise-campaign-signalinformation"></a>

Information about a signal\.

## Syntax<a name="aws-properties-iotfleetwise-campaign-signalinformation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-campaign-signalinformation-syntax.json"></a>

```
{
  "[MaxSampleCount](#cfn-iotfleetwise-campaign-signalinformation-maxsamplecount)" : Double,
  "[MinimumSamplingIntervalMs](#cfn-iotfleetwise-campaign-signalinformation-minimumsamplingintervalms)" : Double,
  "[Name](#cfn-iotfleetwise-campaign-signalinformation-name)" : String
}
```

### YAML<a name="aws-properties-iotfleetwise-campaign-signalinformation-syntax.yaml"></a>

```
  [MaxSampleCount](#cfn-iotfleetwise-campaign-signalinformation-maxsamplecount): Double
  [MinimumSamplingIntervalMs](#cfn-iotfleetwise-campaign-signalinformation-minimumsamplingintervalms): Double
  [Name](#cfn-iotfleetwise-campaign-signalinformation-name): String
```

## Properties<a name="aws-properties-iotfleetwise-campaign-signalinformation-properties"></a>

`MaxSampleCount`  <a name="cfn-iotfleetwise-campaign-signalinformation-maxsamplecount"></a>
The maximum number of samples to collect\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumSamplingIntervalMs`  <a name="cfn-iotfleetwise-campaign-signalinformation-minimumsamplingintervalms"></a>
The minimum duration of time \(in milliseconds\) between two triggering events to collect data\.  
If a signal changes often, you might want to collect data at a slower rate\.
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotfleetwise-campaign-signalinformation-name"></a>
The name of the signal\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `150`  
*Pattern*: `[\w|*|-]+(\.[\w|*|-]+)*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)