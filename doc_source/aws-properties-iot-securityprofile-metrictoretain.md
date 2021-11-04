# AWS::IoT::SecurityProfile MetricToRetain<a name="aws-properties-iot-securityprofile-metrictoretain"></a>

The metric you want to retain\. Dimensions are optional\.

## Syntax<a name="aws-properties-iot-securityprofile-metrictoretain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-securityprofile-metrictoretain-syntax.json"></a>

```
{
  "[Metric](#cfn-iot-securityprofile-metrictoretain-metric)" : String,
  "[MetricDimension](#cfn-iot-securityprofile-metrictoretain-metricdimension)" : MetricDimension
}
```

### YAML<a name="aws-properties-iot-securityprofile-metrictoretain-syntax.yaml"></a>

```
  [Metric](#cfn-iot-securityprofile-metrictoretain-metric): String
  [MetricDimension](#cfn-iot-securityprofile-metrictoretain-metricdimension): 
    MetricDimension
```

## Properties<a name="aws-properties-iot-securityprofile-metrictoretain-properties"></a>

`Metric`  <a name="cfn-iot-securityprofile-metrictoretain-metric"></a>
A standard of measurement\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricDimension`  <a name="cfn-iot-securityprofile-metrictoretain-metricdimension"></a>
The dimension of the metric\.  
*Required*: No  
*Type*: [MetricDimension](aws-properties-iot-securityprofile-metricdimension.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)