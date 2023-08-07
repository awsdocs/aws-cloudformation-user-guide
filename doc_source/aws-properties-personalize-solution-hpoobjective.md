# AWS::Personalize::Solution HpoObjective<a name="aws-properties-personalize-solution-hpoobjective"></a>

The metric to optimize during hyperparameter optimization \(HPO\)\.

**Note**  
Amazon Personalize doesn't support configuring the `hpoObjective` at this time\.

## Syntax<a name="aws-properties-personalize-solution-hpoobjective-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-personalize-solution-hpoobjective-syntax.json"></a>

```
{
  "[MetricName](#cfn-personalize-solution-hpoobjective-metricname)" : String,
  "[MetricRegex](#cfn-personalize-solution-hpoobjective-metricregex)" : String,
  "[Type](#cfn-personalize-solution-hpoobjective-type)" : String
}
```

### YAML<a name="aws-properties-personalize-solution-hpoobjective-syntax.yaml"></a>

```
  [MetricName](#cfn-personalize-solution-hpoobjective-metricname): String
  [MetricRegex](#cfn-personalize-solution-hpoobjective-metricregex): String
  [Type](#cfn-personalize-solution-hpoobjective-type): String
```

## Properties<a name="aws-properties-personalize-solution-hpoobjective-properties"></a>

`MetricName`  <a name="cfn-personalize-solution-hpoobjective-metricname"></a>
The name of the metric\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MetricRegex`  <a name="cfn-personalize-solution-hpoobjective-metricregex"></a>
A regular expression for finding the metric in the training job logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-personalize-solution-hpoobjective-type"></a>
The type of the metric\. Valid values are `Maximize` and `Minimize`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)