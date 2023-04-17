# AWS::QuickSight::Analysis GaugeChartFieldWells<a name="aws-properties-quicksight-analysis-gaugechartfieldwells"></a>

The field well configuration of a `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-gaugechartfieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-gaugechartfieldwells-syntax.json"></a>

```
{
  "[TargetValues](#cfn-quicksight-analysis-gaugechartfieldwells-targetvalues)" : [ MeasureField, ... ],
  "[Values](#cfn-quicksight-analysis-gaugechartfieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-gaugechartfieldwells-syntax.yaml"></a>

```
  [TargetValues](#cfn-quicksight-analysis-gaugechartfieldwells-targetvalues): 
    - MeasureField
  [Values](#cfn-quicksight-analysis-gaugechartfieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-gaugechartfieldwells-properties"></a>

`TargetValues`  <a name="cfn-quicksight-analysis-gaugechartfieldwells-targetvalues"></a>
The target value field wells of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-gaugechartfieldwells-values"></a>
The value field wells of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)