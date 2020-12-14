# AWS::Pinpoint::Campaign MetricDimension<a name="aws-properties-pinpoint-campaign-metricdimension"></a>

Specifies metric\-based criteria for including or excluding endpoints from a segment\. These criteria derive from custom metrics that you define for endpoints\.

## Syntax<a name="aws-properties-pinpoint-campaign-metricdimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpoint-campaign-metricdimension-syntax.json"></a>

```
{
  "[ComparisonOperator](#cfn-pinpoint-campaign-metricdimension-comparisonoperator)" : String,
  "[Value](#cfn-pinpoint-campaign-metricdimension-value)" : Double
}
```

### YAML<a name="aws-properties-pinpoint-campaign-metricdimension-syntax.yaml"></a>

```
  [ComparisonOperator](#cfn-pinpoint-campaign-metricdimension-comparisonoperator): String
  [Value](#cfn-pinpoint-campaign-metricdimension-value): Double
```

## Properties<a name="aws-properties-pinpoint-campaign-metricdimension-properties"></a>

`ComparisonOperator`  <a name="cfn-pinpoint-campaign-metricdimension-comparisonoperator"></a>
The operator to use when comparing metric values\. Valid values are: `GREATER_THAN`, `LESS_THAN`, `GREATER_THAN_OR_EQUAL`, `LESS_THAN_OR_EQUAL`, and `EQUAL`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-pinpoint-campaign-metricdimension-value"></a>
The value to compare\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)