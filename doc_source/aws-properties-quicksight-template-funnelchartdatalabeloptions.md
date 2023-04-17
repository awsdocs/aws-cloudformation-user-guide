# AWS::QuickSight::Template FunnelChartDataLabelOptions<a name="aws-properties-quicksight-template-funnelchartdatalabeloptions"></a>

The options that determine the presentation of the data labels\.

## Syntax<a name="aws-properties-quicksight-template-funnelchartdatalabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-funnelchartdatalabeloptions-syntax.json"></a>

```
{
  "[CategoryLabelVisibility](#cfn-quicksight-template-funnelchartdatalabeloptions-categorylabelvisibility)" : String,
  "[LabelColor](#cfn-quicksight-template-funnelchartdatalabeloptions-labelcolor)" : String,
  "[LabelFontConfiguration](#cfn-quicksight-template-funnelchartdatalabeloptions-labelfontconfiguration)" : FontConfiguration,
  "[MeasureDataLabelStyle](#cfn-quicksight-template-funnelchartdatalabeloptions-measuredatalabelstyle)" : String,
  "[MeasureLabelVisibility](#cfn-quicksight-template-funnelchartdatalabeloptions-measurelabelvisibility)" : String,
  "[Position](#cfn-quicksight-template-funnelchartdatalabeloptions-position)" : String,
  "[Visibility](#cfn-quicksight-template-funnelchartdatalabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-funnelchartdatalabeloptions-syntax.yaml"></a>

```
  [CategoryLabelVisibility](#cfn-quicksight-template-funnelchartdatalabeloptions-categorylabelvisibility): String
  [LabelColor](#cfn-quicksight-template-funnelchartdatalabeloptions-labelcolor): String
  [LabelFontConfiguration](#cfn-quicksight-template-funnelchartdatalabeloptions-labelfontconfiguration): 
    FontConfiguration
  [MeasureDataLabelStyle](#cfn-quicksight-template-funnelchartdatalabeloptions-measuredatalabelstyle): String
  [MeasureLabelVisibility](#cfn-quicksight-template-funnelchartdatalabeloptions-measurelabelvisibility): String
  [Position](#cfn-quicksight-template-funnelchartdatalabeloptions-position): String
  [Visibility](#cfn-quicksight-template-funnelchartdatalabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-funnelchartdatalabeloptions-properties"></a>

`CategoryLabelVisibility`  <a name="cfn-quicksight-template-funnelchartdatalabeloptions-categorylabelvisibility"></a>
The visibility of the category labels within the data labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelColor`  <a name="cfn-quicksight-template-funnelchartdatalabeloptions-labelcolor"></a>
The color of the data label text\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelFontConfiguration`  <a name="cfn-quicksight-template-funnelchartdatalabeloptions-labelfontconfiguration"></a>
The font configuration for the data labels\.  
Only the `FontSize` attribute of the font configuration is used for data labels\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MeasureDataLabelStyle`  <a name="cfn-quicksight-template-funnelchartdatalabeloptions-measuredatalabelstyle"></a>
Determines the style of the metric labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PERCENTAGE_BY_FIRST_STAGE | PERCENTAGE_BY_PREVIOUS_STAGE | VALUE_AND_PERCENTAGE_BY_FIRST_STAGE | VALUE_AND_PERCENTAGE_BY_PREVIOUS_STAGE | VALUE_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MeasureLabelVisibility`  <a name="cfn-quicksight-template-funnelchartdatalabeloptions-measurelabelvisibility"></a>
The visibility of the measure labels within the data labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-quicksight-template-funnelchartdatalabeloptions-position"></a>
Determines the positioning of the data label relative to a section of the funnel\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BOTTOM | INSIDE | LEFT | OUTSIDE | RIGHT | TOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-funnelchartdatalabeloptions-visibility"></a>
The visibility option that determines if data labels are displayed\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)