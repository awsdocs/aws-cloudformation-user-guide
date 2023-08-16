# AWS::QuickSight::Dashboard DateTimePickerControlDisplayOptions<a name="aws-properties-quicksight-dashboard-datetimepickercontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-dashboard-datetimepickercontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-datetimepickercontroldisplayoptions-syntax.json"></a>

```
{
  "[DateTimeFormat](#cfn-quicksight-dashboard-datetimepickercontroldisplayoptions-datetimeformat)" : String,
  "[TitleOptions](#cfn-quicksight-dashboard-datetimepickercontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-datetimepickercontroldisplayoptions-syntax.yaml"></a>

```
  [DateTimeFormat](#cfn-quicksight-dashboard-datetimepickercontroldisplayoptions-datetimeformat): String
  [TitleOptions](#cfn-quicksight-dashboard-datetimepickercontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-datetimepickercontroldisplayoptions-properties"></a>

`DateTimeFormat`  <a name="cfn-quicksight-dashboard-datetimepickercontroldisplayoptions-datetimeformat"></a>
Customize how dates are formatted in controls\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-dashboard-datetimepickercontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-dashboard-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)