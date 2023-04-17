# AWS::QuickSight::Analysis ArcOptions<a name="aws-properties-quicksight-analysis-arcoptions"></a>

The options that determine the arc thickness of a `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-arcoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-arcoptions-syntax.json"></a>

```
{
  "[ArcThickness](#cfn-quicksight-analysis-arcoptions-arcthickness)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-arcoptions-syntax.yaml"></a>

```
  [ArcThickness](#cfn-quicksight-analysis-arcoptions-arcthickness): String
```

## Properties<a name="aws-properties-quicksight-analysis-arcoptions-properties"></a>

`ArcThickness`  <a name="cfn-quicksight-analysis-arcoptions-arcthickness"></a>
The arc thickness of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LARGE | MEDIUM | SMALL | WHOLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)