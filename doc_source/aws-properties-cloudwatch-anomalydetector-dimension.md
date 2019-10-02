# AWS::CloudWatch::AnomalyDetector Dimension<a name="aws-properties-cloudwatch-anomalydetector-dimension"></a>

Expands the identity of a metric\.

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
The value representing the dimension measurement\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Supported Regions

This PropertyType is supported by ***all*** regions.