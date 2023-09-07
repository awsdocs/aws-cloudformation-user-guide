# AWS::QuickSight::Analysis DateTimePickerControlDisplayOptions<a name="aws-properties-quicksight-analysis-datetimepickercontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-analysis-datetimepickercontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-datetimepickercontroldisplayoptions-syntax.json"></a>

```
{
  "[DateTimeFormat](#cfn-quicksight-analysis-datetimepickercontroldisplayoptions-datetimeformat)" : String,
  "[InfoIconLabelOptions](#cfn-quicksight-analysis-datetimepickercontroldisplayoptions-infoiconlabeloptions)" : SheetControlInfoIconLabelOptions,
  "[TitleOptions](#cfn-quicksight-analysis-datetimepickercontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-datetimepickercontroldisplayoptions-syntax.yaml"></a>

```
  [DateTimeFormat](#cfn-quicksight-analysis-datetimepickercontroldisplayoptions-datetimeformat): String
  [InfoIconLabelOptions](#cfn-quicksight-analysis-datetimepickercontroldisplayoptions-infoiconlabeloptions): 
    SheetControlInfoIconLabelOptions
  [TitleOptions](#cfn-quicksight-analysis-datetimepickercontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-datetimepickercontroldisplayoptions-properties"></a>

`DateTimeFormat`  <a name="cfn-quicksight-analysis-datetimepickercontroldisplayoptions-datetimeformat"></a>
Customize how dates are formatted in controls\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InfoIconLabelOptions`  <a name="cfn-quicksight-analysis-datetimepickercontroldisplayoptions-infoiconlabeloptions"></a>
The configuration of info icon label options\.  
*Required*: No  
*Type*: [SheetControlInfoIconLabelOptions](aws-properties-quicksight-analysis-sheetcontrolinfoiconlabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-analysis-datetimepickercontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-analysis-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)