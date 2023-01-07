# AWS::IoT::SecurityProfile Behavior<a name="aws-properties-iot-securityprofile-behavior"></a>

A Device Defender security profile behavior\.

## Syntax<a name="aws-properties-iot-securityprofile-behavior-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-securityprofile-behavior-syntax.json"></a>

```
{
  "[Criteria](#cfn-iot-securityprofile-behavior-criteria)" : BehaviorCriteria,
  "[Metric](#cfn-iot-securityprofile-behavior-metric)" : String,
  "[MetricDimension](#cfn-iot-securityprofile-behavior-metricdimension)" : MetricDimension,
  "[Name](#cfn-iot-securityprofile-behavior-name)" : String,
  "[SuppressAlerts](#cfn-iot-securityprofile-behavior-suppressalerts)" : Boolean
}
```

### YAML<a name="aws-properties-iot-securityprofile-behavior-syntax.yaml"></a>

```
  [Criteria](#cfn-iot-securityprofile-behavior-criteria): 
    BehaviorCriteria
  [Metric](#cfn-iot-securityprofile-behavior-metric): String
  [MetricDimension](#cfn-iot-securityprofile-behavior-metricdimension): 
    MetricDimension
  [Name](#cfn-iot-securityprofile-behavior-name): String
  [SuppressAlerts](#cfn-iot-securityprofile-behavior-suppressalerts): Boolean
```

## Properties<a name="aws-properties-iot-securityprofile-behavior-properties"></a>

`Criteria`  <a name="cfn-iot-securityprofile-behavior-criteria"></a>
The criteria that determine if a device is behaving normally in regard to the `metric`\.  
*Required*: No  
*Type*: [BehaviorCriteria](aws-properties-iot-securityprofile-behaviorcriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Metric`  <a name="cfn-iot-securityprofile-behavior-metric"></a>
What is measured by the behavior\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricDimension`  <a name="cfn-iot-securityprofile-behavior-metricdimension"></a>
The dimension of the metric\.  
*Required*: No  
*Type*: [MetricDimension](aws-properties-iot-securityprofile-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iot-securityprofile-behavior-name"></a>
The name you've given to the behavior\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuppressAlerts`  <a name="cfn-iot-securityprofile-behavior-suppressalerts"></a>
The alert status\. If you set the value to `true`, alerts will be suppressed\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)