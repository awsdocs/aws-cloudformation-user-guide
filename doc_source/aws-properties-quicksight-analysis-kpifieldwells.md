# AWS::QuickSight::Analysis KPIFieldWells<a name="aws-properties-quicksight-analysis-kpifieldwells"></a>

The field well configuration of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-analysis-kpifieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-kpifieldwells-syntax.json"></a>

```
{
  "[TargetValues](#cfn-quicksight-analysis-kpifieldwells-targetvalues)" : [ MeasureField, ... ],
  "[TrendGroups](#cfn-quicksight-analysis-kpifieldwells-trendgroups)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-analysis-kpifieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-kpifieldwells-syntax.yaml"></a>

```
  [TargetValues](#cfn-quicksight-analysis-kpifieldwells-targetvalues): 
    - MeasureField
  [TrendGroups](#cfn-quicksight-analysis-kpifieldwells-trendgroups): 
    - DimensionField
  [Values](#cfn-quicksight-analysis-kpifieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-analysis-kpifieldwells-properties"></a>

`TargetValues`  <a name="cfn-quicksight-analysis-kpifieldwells-targetvalues"></a>
The target value field wells of a KPI visual\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrendGroups`  <a name="cfn-quicksight-analysis-kpifieldwells-trendgroups"></a>
The trend group field wells of a KPI visual\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-analysis-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-analysis-kpifieldwells-values"></a>
The value field wells of a KPI visual\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-analysis-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)