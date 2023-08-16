# AWS::QuickSight::Analysis ArcConfiguration<a name="aws-properties-quicksight-analysis-arcconfiguration"></a>

The arc configuration of a `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-arcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-arcconfiguration-syntax.json"></a>

```
{
  "[ArcAngle](#cfn-quicksight-analysis-arcconfiguration-arcangle)" : Double,
  "[ArcThickness](#cfn-quicksight-analysis-arcconfiguration-arcthickness)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-arcconfiguration-syntax.yaml"></a>

```
  [ArcAngle](#cfn-quicksight-analysis-arcconfiguration-arcangle): Double
  [ArcThickness](#cfn-quicksight-analysis-arcconfiguration-arcthickness): String
```

## Properties<a name="aws-properties-quicksight-analysis-arcconfiguration-properties"></a>

`ArcAngle`  <a name="cfn-quicksight-analysis-arcconfiguration-arcangle"></a>
The option that determines the arc angle of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ArcThickness`  <a name="cfn-quicksight-analysis-arcconfiguration-arcthickness"></a>
The options that determine the arc thickness of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LARGE | MEDIUM | SMALL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)