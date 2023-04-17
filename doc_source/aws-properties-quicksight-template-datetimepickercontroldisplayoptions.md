# AWS::QuickSight::Template DateTimePickerControlDisplayOptions<a name="aws-properties-quicksight-template-datetimepickercontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-template-datetimepickercontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-datetimepickercontroldisplayoptions-syntax.json"></a>

```
{
  "[DateTimeFormat](#cfn-quicksight-template-datetimepickercontroldisplayoptions-datetimeformat)" : String,
  "[TitleOptions](#cfn-quicksight-template-datetimepickercontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-template-datetimepickercontroldisplayoptions-syntax.yaml"></a>

```
  [DateTimeFormat](#cfn-quicksight-template-datetimepickercontroldisplayoptions-datetimeformat): String
  [TitleOptions](#cfn-quicksight-template-datetimepickercontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-template-datetimepickercontroldisplayoptions-properties"></a>

`DateTimeFormat`  <a name="cfn-quicksight-template-datetimepickercontroldisplayoptions-datetimeformat"></a>
Customize how dates are formatted in controls\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-template-datetimepickercontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-template-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)