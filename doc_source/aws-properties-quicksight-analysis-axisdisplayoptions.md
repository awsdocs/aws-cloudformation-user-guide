# AWS::QuickSight::Analysis AxisDisplayOptions<a name="aws-properties-quicksight-analysis-axisdisplayoptions"></a>

The display options for the axis label\.

## Syntax<a name="aws-properties-quicksight-analysis-axisdisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-axisdisplayoptions-syntax.json"></a>

```
{
  "[AxisLineVisibility](#cfn-quicksight-analysis-axisdisplayoptions-axislinevisibility)" : String,
  "[AxisOffset](#cfn-quicksight-analysis-axisdisplayoptions-axisoffset)" : String,
  "[DataOptions](#cfn-quicksight-analysis-axisdisplayoptions-dataoptions)" : AxisDataOptions,
  "[GridLineVisibility](#cfn-quicksight-analysis-axisdisplayoptions-gridlinevisibility)" : String,
  "[ScrollbarOptions](#cfn-quicksight-analysis-axisdisplayoptions-scrollbaroptions)" : ScrollBarOptions,
  "[TickLabelOptions](#cfn-quicksight-analysis-axisdisplayoptions-ticklabeloptions)" : AxisTickLabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-axisdisplayoptions-syntax.yaml"></a>

```
  [AxisLineVisibility](#cfn-quicksight-analysis-axisdisplayoptions-axislinevisibility): String
  [AxisOffset](#cfn-quicksight-analysis-axisdisplayoptions-axisoffset): String
  [DataOptions](#cfn-quicksight-analysis-axisdisplayoptions-dataoptions): 
    AxisDataOptions
  [GridLineVisibility](#cfn-quicksight-analysis-axisdisplayoptions-gridlinevisibility): String
  [ScrollbarOptions](#cfn-quicksight-analysis-axisdisplayoptions-scrollbaroptions): 
    ScrollBarOptions
  [TickLabelOptions](#cfn-quicksight-analysis-axisdisplayoptions-ticklabeloptions): 
    AxisTickLabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-axisdisplayoptions-properties"></a>

`AxisLineVisibility`  <a name="cfn-quicksight-analysis-axisdisplayoptions-axislinevisibility"></a>
Determines whether or not the axis line is visible\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AxisOffset`  <a name="cfn-quicksight-analysis-axisdisplayoptions-axisoffset"></a>
The offset value that determines the starting placement of the axis within a visual's bounds\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataOptions`  <a name="cfn-quicksight-analysis-axisdisplayoptions-dataoptions"></a>
The data options for an axis\.  
*Required*: No  
*Type*: [AxisDataOptions](aws-properties-quicksight-analysis-axisdataoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GridLineVisibility`  <a name="cfn-quicksight-analysis-axisdisplayoptions-gridlinevisibility"></a>
Determines whether or not the grid line is visible\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScrollbarOptions`  <a name="cfn-quicksight-analysis-axisdisplayoptions-scrollbaroptions"></a>
The scroll bar options for an axis\.  
*Required*: No  
*Type*: [ScrollBarOptions](aws-properties-quicksight-analysis-scrollbaroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TickLabelOptions`  <a name="cfn-quicksight-analysis-axisdisplayoptions-ticklabeloptions"></a>
The tick label options of an axis\.  
*Required*: No  
*Type*: [AxisTickLabelOptions](aws-properties-quicksight-analysis-axisticklabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)