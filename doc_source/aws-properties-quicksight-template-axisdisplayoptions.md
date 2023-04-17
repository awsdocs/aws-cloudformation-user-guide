# AWS::QuickSight::Template AxisDisplayOptions<a name="aws-properties-quicksight-template-axisdisplayoptions"></a>

The display options for the axis label\.

## Syntax<a name="aws-properties-quicksight-template-axisdisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-axisdisplayoptions-syntax.json"></a>

```
{
  "[AxisLineVisibility](#cfn-quicksight-template-axisdisplayoptions-axislinevisibility)" : String,
  "[AxisOffset](#cfn-quicksight-template-axisdisplayoptions-axisoffset)" : String,
  "[DataOptions](#cfn-quicksight-template-axisdisplayoptions-dataoptions)" : AxisDataOptions,
  "[GridLineVisibility](#cfn-quicksight-template-axisdisplayoptions-gridlinevisibility)" : String,
  "[ScrollbarOptions](#cfn-quicksight-template-axisdisplayoptions-scrollbaroptions)" : ScrollBarOptions,
  "[TickLabelOptions](#cfn-quicksight-template-axisdisplayoptions-ticklabeloptions)" : AxisTickLabelOptions
}
```

### YAML<a name="aws-properties-quicksight-template-axisdisplayoptions-syntax.yaml"></a>

```
  [AxisLineVisibility](#cfn-quicksight-template-axisdisplayoptions-axislinevisibility): String
  [AxisOffset](#cfn-quicksight-template-axisdisplayoptions-axisoffset): String
  [DataOptions](#cfn-quicksight-template-axisdisplayoptions-dataoptions): 
    AxisDataOptions
  [GridLineVisibility](#cfn-quicksight-template-axisdisplayoptions-gridlinevisibility): String
  [ScrollbarOptions](#cfn-quicksight-template-axisdisplayoptions-scrollbaroptions): 
    ScrollBarOptions
  [TickLabelOptions](#cfn-quicksight-template-axisdisplayoptions-ticklabeloptions): 
    AxisTickLabelOptions
```

## Properties<a name="aws-properties-quicksight-template-axisdisplayoptions-properties"></a>

`AxisLineVisibility`  <a name="cfn-quicksight-template-axisdisplayoptions-axislinevisibility"></a>
Determines whether or not the axis line is visible\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AxisOffset`  <a name="cfn-quicksight-template-axisdisplayoptions-axisoffset"></a>
The offset value that determines the starting placement of the axis within a visual's bounds\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataOptions`  <a name="cfn-quicksight-template-axisdisplayoptions-dataoptions"></a>
The data options for an axis\.  
*Required*: No  
*Type*: [AxisDataOptions](aws-properties-quicksight-template-axisdataoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GridLineVisibility`  <a name="cfn-quicksight-template-axisdisplayoptions-gridlinevisibility"></a>
Determines whether or not the grid line is visible\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScrollbarOptions`  <a name="cfn-quicksight-template-axisdisplayoptions-scrollbaroptions"></a>
The scroll bar options for an axis\.  
*Required*: No  
*Type*: [ScrollBarOptions](aws-properties-quicksight-template-scrollbaroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TickLabelOptions`  <a name="cfn-quicksight-template-axisdisplayoptions-ticklabeloptions"></a>
The tick label options of an axis\.  
*Required*: No  
*Type*: [AxisTickLabelOptions](aws-properties-quicksight-template-axisticklabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)