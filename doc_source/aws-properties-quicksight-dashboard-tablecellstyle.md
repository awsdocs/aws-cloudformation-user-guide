# AWS::QuickSight::Dashboard TableCellStyle<a name="aws-properties-quicksight-dashboard-tablecellstyle"></a>

The table cell style for a cell in pivot table or table visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-tablecellstyle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-tablecellstyle-syntax.json"></a>

```
{
  "[BackgroundColor](#cfn-quicksight-dashboard-tablecellstyle-backgroundcolor)" : String,
  "[Border](#cfn-quicksight-dashboard-tablecellstyle-border)" : GlobalTableBorderOptions,
  "[FontConfiguration](#cfn-quicksight-dashboard-tablecellstyle-fontconfiguration)" : FontConfiguration,
  "[Height](#cfn-quicksight-dashboard-tablecellstyle-height)" : Double,
  "[HorizontalTextAlignment](#cfn-quicksight-dashboard-tablecellstyle-horizontaltextalignment)" : String,
  "[TextWrap](#cfn-quicksight-dashboard-tablecellstyle-textwrap)" : String,
  "[VerticalTextAlignment](#cfn-quicksight-dashboard-tablecellstyle-verticaltextalignment)" : String,
  "[Visibility](#cfn-quicksight-dashboard-tablecellstyle-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-tablecellstyle-syntax.yaml"></a>

```
  [BackgroundColor](#cfn-quicksight-dashboard-tablecellstyle-backgroundcolor): String
  [Border](#cfn-quicksight-dashboard-tablecellstyle-border): 
    GlobalTableBorderOptions
  [FontConfiguration](#cfn-quicksight-dashboard-tablecellstyle-fontconfiguration): 
    FontConfiguration
  [Height](#cfn-quicksight-dashboard-tablecellstyle-height): Double
  [HorizontalTextAlignment](#cfn-quicksight-dashboard-tablecellstyle-horizontaltextalignment): String
  [TextWrap](#cfn-quicksight-dashboard-tablecellstyle-textwrap): String
  [VerticalTextAlignment](#cfn-quicksight-dashboard-tablecellstyle-verticaltextalignment): String
  [Visibility](#cfn-quicksight-dashboard-tablecellstyle-visibility): String
```

## Properties<a name="aws-properties-quicksight-dashboard-tablecellstyle-properties"></a>

`BackgroundColor`  <a name="cfn-quicksight-dashboard-tablecellstyle-backgroundcolor"></a>
The background color for the table cells\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Border`  <a name="cfn-quicksight-dashboard-tablecellstyle-border"></a>
The borders for the table cells\.  
*Required*: No  
*Type*: [GlobalTableBorderOptions](aws-properties-quicksight-dashboard-globaltableborderoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FontConfiguration`  <a name="cfn-quicksight-dashboard-tablecellstyle-fontconfiguration"></a>
The font configuration of the table cells\.  
*Required*: No  
*Type*: [FontConfiguration](aws-properties-quicksight-dashboard-fontconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Height`  <a name="cfn-quicksight-dashboard-tablecellstyle-height"></a>
The height color for the table cells\.  
*Required*: No  
*Type*: Double  
*Minimum*: `8`  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HorizontalTextAlignment`  <a name="cfn-quicksight-dashboard-tablecellstyle-horizontaltextalignment"></a>
The horizontal text alignment \(left, center, right, auto\) for the table cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | CENTER | LEFT | RIGHT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextWrap`  <a name="cfn-quicksight-dashboard-tablecellstyle-textwrap"></a>
The text wrap \(none, wrap\) for the table cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | WRAP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerticalTextAlignment`  <a name="cfn-quicksight-dashboard-tablecellstyle-verticaltextalignment"></a>
The vertical text alignment \(top, middle, bottom\) for the table cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTO | BOTTOM | MIDDLE | TOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-tablecellstyle-visibility"></a>
The visibility of the table cells\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)