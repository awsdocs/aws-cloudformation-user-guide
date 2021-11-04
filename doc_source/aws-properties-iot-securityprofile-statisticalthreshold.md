# AWS::IoT::SecurityProfile StatisticalThreshold<a name="aws-properties-iot-securityprofile-statisticalthreshold"></a>

A statistical ranking \(percentile\) that indicates a threshold value by which a behavior is determined to be in compliance or in violation of the behavior\.

## Syntax<a name="aws-properties-iot-securityprofile-statisticalthreshold-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-securityprofile-statisticalthreshold-syntax.json"></a>

```
{
  "[Statistic](#cfn-iot-securityprofile-statisticalthreshold-statistic)" : String
}
```

### YAML<a name="aws-properties-iot-securityprofile-statisticalthreshold-syntax.yaml"></a>

```
  [Statistic](#cfn-iot-securityprofile-statisticalthreshold-statistic): String
```

## Properties<a name="aws-properties-iot-securityprofile-statisticalthreshold-properties"></a>

`Statistic`  <a name="cfn-iot-securityprofile-statisticalthreshold-statistic"></a>
The percentile that resolves to a threshold value by which compliance with a behavior is determined\. Metrics are collected over the specified period \(`durationSeconds`\) from all reporting devices in your account and statistical ranks are calculated\. Then, the measurements from a device are collected over the same period\. If the accumulated measurements from the device fall above or below \(`comparisonOperator`\) the value associated with the percentile specified, then the device is considered to be in compliance with the behavior, otherwise a violation occurs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)