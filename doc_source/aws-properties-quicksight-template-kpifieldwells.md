# AWS::QuickSight::Template KPIFieldWells<a name="aws-properties-quicksight-template-kpifieldwells"></a>

The field well configuration of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-template-kpifieldwells-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-kpifieldwells-syntax.json"></a>

```
{
  "[TargetValues](#cfn-quicksight-template-kpifieldwells-targetvalues)" : [ MeasureField, ... ],
  "[TrendGroups](#cfn-quicksight-template-kpifieldwells-trendgroups)" : [ DimensionField, ... ],
  "[Values](#cfn-quicksight-template-kpifieldwells-values)" : [ MeasureField, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-kpifieldwells-syntax.yaml"></a>

```
  [TargetValues](#cfn-quicksight-template-kpifieldwells-targetvalues): 
    - MeasureField
  [TrendGroups](#cfn-quicksight-template-kpifieldwells-trendgroups): 
    - DimensionField
  [Values](#cfn-quicksight-template-kpifieldwells-values): 
    - MeasureField
```

## Properties<a name="aws-properties-quicksight-template-kpifieldwells-properties"></a>

`TargetValues`  <a name="cfn-quicksight-template-kpifieldwells-targetvalues"></a>
The target value field wells of a KPI visual\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrendGroups`  <a name="cfn-quicksight-template-kpifieldwells-trendgroups"></a>
The trend group field wells of a KPI visual\.  
*Required*: No  
*Type*: List of [DimensionField](aws-properties-quicksight-template-dimensionfield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-quicksight-template-kpifieldwells-values"></a>
The value field wells of a KPI visual\.  
*Required*: No  
*Type*: List of [MeasureField](aws-properties-quicksight-template-measurefield.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)