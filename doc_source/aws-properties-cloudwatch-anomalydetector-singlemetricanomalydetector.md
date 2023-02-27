# AWS::CloudWatch::AnomalyDetector SingleMetricAnomalyDetector<a name="aws-properties-cloudwatch-anomalydetector-singlemetricanomalydetector"></a>

Designates the CloudWatch metric and statistic that provides the time series the anomaly detector uses as input\.

## Syntax<a name="aws-properties-cloudwatch-anomalydetector-singlemetricanomalydetector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-anomalydetector-singlemetricanomalydetector-syntax.json"></a>

```
{
  "[Dimensions](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-dimensions)" : [ Dimension, ... ],
  "[MetricName](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-metricname)" : String,
  "[Namespace](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-namespace)" : String,
  "[Stat](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-stat)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-anomalydetector-singlemetricanomalydetector-syntax.yaml"></a>

```
  [Dimensions](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-dimensions): 
    - Dimension
  [MetricName](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-metricname): String
  [Namespace](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-namespace): String
  [Stat](#cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-stat): String
```

## Properties<a name="aws-properties-cloudwatch-anomalydetector-singlemetricanomalydetector-properties"></a>

`Dimensions`  <a name="cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-dimensions"></a>
The metric dimensions to create the anomaly detection model for\.  
*Required*: No  
*Type*: List of [Dimension](aws-properties-cloudwatch-anomalydetector-dimension.md)  
*Maximum*: `30`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MetricName`  <a name="cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-metricname"></a>
The name of the metric to create the anomaly detection model for\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Namespace`  <a name="cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-namespace"></a>
The namespace of the metric to create the anomaly detection model for\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[^:].*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Stat`  <a name="cfn-cloudwatch-anomalydetector-singlemetricanomalydetector-stat"></a>
The statistic to use for the metric and anomaly detection model\.  
*Required*: No  
*Type*: String  
*Maximum*: `50`  
*Pattern*: `(SampleCount|Average|Sum|Minimum|Maximum|IQM|(p|tc|tm|ts|wm)(\d{1,2}(\.\d{0,10})?|100)|[ou]\d+(\.\d*)?)(_E|_L|_H)?|(TM|TC|TS|WM)\(((((\d{1,2})(\.\d{0,10})?|100(\.0{0,10})?)%)?:((\d{1,2})(\.\d{0,10})?|100(\.0{0,10})?)%|((\d{1,2})(\.\d{0,10})?|100(\.0{0,10})?)%:(((\d{1,2})(\.\d{0,10})?|100(\.0{0,10})?)%)?)\)|(TM|TC|TS|WM|PR)\(((\d+(\.\d{0,10})?|(\d+(\.\d{0,10})?[Ee][+-]?\d+)):((\d+(\.\d{0,10})?|(\d+(\.\d{0,10})?[Ee][+-]?\d+)))?|((\d+(\.\d{0,10})?|(\d+(\.\d{0,10})?[Ee][+-]?\d+)))?:(\d+(\.\d{0,10})?|(\d+(\.\d{0,10})?[Ee][+-]?\d+)))\)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)