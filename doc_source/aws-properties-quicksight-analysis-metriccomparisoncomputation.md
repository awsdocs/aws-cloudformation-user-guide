# AWS::QuickSight::Analysis MetricComparisonComputation<a name="aws-properties-quicksight-analysis-metriccomparisoncomputation"></a>

The metric comparison computation configuration\.

## Syntax<a name="aws-properties-quicksight-analysis-metriccomparisoncomputation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-metriccomparisoncomputation-syntax.json"></a>

```
{
  "[ComputationId](#cfn-quicksight-analysis-metriccomparisoncomputation-computationid)" : String,
  "[FromValue](#cfn-quicksight-analysis-metriccomparisoncomputation-fromvalue)" : MeasureField,
  "[Name](#cfn-quicksight-analysis-metriccomparisoncomputation-name)" : String,
  "[TargetValue](#cfn-quicksight-analysis-metriccomparisoncomputation-targetvalue)" : MeasureField,
  "[Time](#cfn-quicksight-analysis-metriccomparisoncomputation-time)" : DimensionField
}
```

### YAML<a name="aws-properties-quicksight-analysis-metriccomparisoncomputation-syntax.yaml"></a>

```
  [ComputationId](#cfn-quicksight-analysis-metriccomparisoncomputation-computationid): String
  [FromValue](#cfn-quicksight-analysis-metriccomparisoncomputation-fromvalue): 
    MeasureField
  [Name](#cfn-quicksight-analysis-metriccomparisoncomputation-name): String
  [TargetValue](#cfn-quicksight-analysis-metriccomparisoncomputation-targetvalue): 
    MeasureField
  [Time](#cfn-quicksight-analysis-metriccomparisoncomputation-time): 
    DimensionField
```

## Properties<a name="aws-properties-quicksight-analysis-metriccomparisoncomputation-properties"></a>

`ComputationId`  <a name="cfn-quicksight-analysis-metriccomparisoncomputation-computationid"></a>
The ID for a computation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FromValue`  <a name="cfn-quicksight-analysis-metriccomparisoncomputation-fromvalue"></a>
The field that is used in a metric comparison from value setup\.  
*Required*: Yes  
*Type*: [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-quicksight-analysis-metriccomparisoncomputation-name"></a>
The name of a computation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetValue`  <a name="cfn-quicksight-analysis-metriccomparisoncomputation-targetvalue"></a>
The field that is used in a metric comparison to value setup\.  
*Required*: Yes  
*Type*: [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Time`  <a name="cfn-quicksight-analysis-metriccomparisoncomputation-time"></a>
The time field that is used in a computation\.  
*Required*: Yes  
*Type*: [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)