# AWS::QuickSight::Template DataLabelOptions<a name="aws-properties-quicksight-template-datalabeloptions"></a>

The options that determine the presentation of the data labels\.

## Syntax<a name="aws-properties-quicksight-template-datalabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-datalabeloptions-syntax.json"></a>

```
{
  "[CategoryLabelVisibility](#cfn-quicksight-template-datalabeloptions-categorylabelvisibility)" : String,
  "[DataLabelTypes](#cfn-quicksight-template-datalabeloptions-datalabeltypes)" : [ DataLabelType, ... ],
  "[LabelColor](#cfn-quicksight-template-datalabeloptions-labelcolor)" : String,
  "[LabelContent](#cfn-quicksight-template-datalabeloptions-labelcontent)" : String,
  "[LabelFontConfiguration](#cfn-quicksight-template-datalabeloptions-labelfontconfiguration)" : FontConfiguration,
  "[MeasureLabelVisibility](#cfn-quicksight-template-datalabeloptions-measurelabelvisibility)" : String,
  "[Overlap](#cfn-quicksight-template-datalabeloptions-overlap)" : String,
  "[Position](#cfn-quicksight-template-datalabeloptions-position)" : String,
  "[Visibility](#cfn-quicksight-template-datalabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-datalabeloptions-syntax.yaml"></a>

```
  [CategoryLabelVisibility](#cfn-quicksight-template-datalabeloptions-categorylabelvisibility): String
  [DataLabelTypes](#cfn-quicksight-template-datalabeloptions-datalabeltypes): 
    - DataLabelType
  [LabelColor](#cfn-quicksight-template-datalabeloptions-labelcolor): String
  [LabelContent](#cfn-quicksight-template-datalabeloptions-labelcontent): String
  [LabelFontConfiguration](#cfn-quicksight-template-datalabeloptions-labelfontconfiguration): 
    FontConfiguration
  [MeasureLabelVisibility](#cfn-quicksight-template-datalabeloptions-measurelabelvisibility): String
  [Overlap](#cfn-quicksight-template-datalabeloptions-overlap): String
  [Position](#cfn-quicksight-template-datalabeloptions-position): String
  [Visibility](#cfn-quicksight-template-datalabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-template-datalabeloptions-properties"></a>

`CategoryLabelVisibility`  <a name="cfn-quicksight-template-datalabeloptions-categorylabelvisibility"></a>
Determines the visibility of the category field labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataLabelTypes`  <a name="cfn-quicksight-template-datalabeloptions-datalabeltypes"></a>
The option that determines the data label type\.  
*Required*: No  
*Type*: List of [DataLabelType](aws-properties-quicksight-template-datalabeltype.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelColor`  <a name="cfn-quicksight-template-datalabeloptions-labelcolor"></a>
Determines the color of the data labels\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelContent`  <a name="cfn-quicksight-template-datalabeloptions-labelcontent"></a>
Determines the content of the data labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PERCENT | VALUE | VALUE_AND_PERCENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelFontConfiguration`  <a name="cfn-quicksight-template-datalabeloptions-labelfontconfiguration"></a>
Determines the font configuration of the data labels\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-template-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MeasureLabelVisibility`  <a name="cfn-quicksight-template-datalabeloptions-measurelabelvisibility"></a>
Determines the visibility of the measure field labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Overlap`  <a name="cfn-quicksight-template-datalabeloptions-overlap"></a>
Determines whether overlap is enabled or disabled for the data labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLE_OVERLAP | ENABLE_OVERLAP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-quicksight-template-datalabeloptions-position"></a>
Determines the position of the data labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BOTTOM | INSIDE | LEFT | OUTSIDE | RIGHT | TOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-datalabeloptions-visibility"></a>
Determines the visibility of the data labels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)