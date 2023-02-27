# AWS::CloudWatch::AnomalyDetector Dimension<a name="aws-properties-cloudwatch-anomalydetector-dimension"></a>

A dimension is a name/value pair that is part of the identity of a metric\. Because dimensions are part of the unique identifier for a metric, whenever you add a unique name/value pair to one of your metrics, you are creating a new variation of that metric\. For example, many Amazon EC2 metrics publish `InstanceId` as a dimension name, and the actual instance ID as the value for that dimension\.

You can assign up to 30 dimensions to a metric\.

## Syntax<a name="aws-properties-cloudwatch-anomalydetector-dimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudwatch-anomalydetector-dimension-syntax.json"></a>

```
{
  "[Name](#cfn-cloudwatch-anomalydetector-dimension-name)" : String,
  "[Value](#cfn-cloudwatch-anomalydetector-dimension-value)" : String
}
```

### YAML<a name="aws-properties-cloudwatch-anomalydetector-dimension-syntax.yaml"></a>

```
  [Name](#cfn-cloudwatch-anomalydetector-dimension-name): String
  [Value](#cfn-cloudwatch-anomalydetector-dimension-value): String
```

## Properties<a name="aws-properties-cloudwatch-anomalydetector-dimension-properties"></a>

`Name`  <a name="cfn-cloudwatch-anomalydetector-dimension-name"></a>
The name of the dimension\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-cloudwatch-anomalydetector-dimension-value"></a>
The value of the dimension\. Dimension values must contain only ASCII characters and must include at least one non\-whitespace character\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)