# AWS::IoT::CustomMetric<a name="aws-resource-iot-custommetric"></a>

 Use the `AWS::IoT::CustomMetric` resource to define a custom metric published by your devices to Device Defender\. For API reference, see [CreateCustomMetric](https://docs.aws.amazon.com/iot/latest/apireference/API_CreateCustomMetric.html) and for general information, see [Custom metrics](https://docs.aws.amazon.com/iot/latest/developerguide/dd-detect-custom-metrics.html)\.

## Syntax<a name="aws-resource-iot-custommetric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-custommetric-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::CustomMetric",
  "Properties" : {
      "[DisplayName](#cfn-iot-custommetric-displayname)" : String,
      "[MetricName](#cfn-iot-custommetric-metricname)" : String,
      "[MetricType](#cfn-iot-custommetric-metrictype)" : String,
      "[Tags](#cfn-iot-custommetric-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iot-custommetric-syntax.yaml"></a>

```
Type: AWS::IoT::CustomMetric
Properties: 
  [DisplayName](#cfn-iot-custommetric-displayname): String
  [MetricName](#cfn-iot-custommetric-metricname): String
  [MetricType](#cfn-iot-custommetric-metrictype): String
  [Tags](#cfn-iot-custommetric-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iot-custommetric-properties"></a>

`DisplayName`  <a name="cfn-iot-custommetric-displayname"></a>
 The friendly name in the console for the custom metric\. This name doesn't have to be unique\. Don't use this name as the metric identifier in the device metric report\. You can update the friendly name after you define it\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-iot-custommetric-metricname"></a>
 The name of the custom metric\. This will be used in the metric report submitted from the device/thing\. The name can't begin with `aws:`\. You can’t change the name after you define it\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MetricType`  <a name="cfn-iot-custommetric-metrictype"></a>
 The type of the custom metric\. Types include `string-list`, `ip-address-list`, `number-list`, and `number`\.   
The type `number` only takes a single metric value as an input, but when you submit the metrics value in the DeviceMetrics report, you must pass it as an array with a single value\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iot-custommetric-tags"></a>
 Metadata that can be used to manage the custom metric\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-custommetric-return-values"></a>

### Ref<a name="aws-resource-iot-custommetric-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the custom metric name\.

### Fn::GetAtt<a name="aws-resource-iot-custommetric-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-custommetric-return-values-fn--getatt-fn--getatt"></a>

`MetricArn`  <a name="MetricArn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) of the custom metric; for example, `arn:aws-partition:iot:region:accountId:custommetric/metricName`\.

## Examples<a name="aws-resource-iot-custommetric--examples"></a>



### <a name="aws-resource-iot-custommetric--examples--"></a>



#### JSON<a name="aws-resource-iot-custommetric--examples----json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Amazon Web Services IoT CustomMetric Sample Template",
  "Resources": {
    "BatteryPercentageMetric": {
      "Type": "AWS::IoT::CustomMetric",
      "Properties": {
        "MetricName": "batteryPercentage",
        "DisplayName": "Remaining battery percentage",
        "MetricType": "number"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-iot-custommetric--examples----yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Amazon Web Services IoT CustomMetric Sample Template
Resources:
  BatteryPercentageMetric:
    Type: AWS::IoT::CustomMetric
    Properties:
      MetricName: batteryPercentage
      DisplayName: Remaining battery percentage
      MetricType: number
```