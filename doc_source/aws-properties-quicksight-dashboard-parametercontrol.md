# AWS::QuickSight::Dashboard ParameterControl<a name="aws-properties-quicksight-dashboard-parametercontrol"></a>

The control of a parameter that users can interact with in a dashboard or an analysis\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-parametercontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-parametercontrol-syntax.json"></a>

```
{
  "[DateTimePicker](#cfn-quicksight-dashboard-parametercontrol-datetimepicker)" : ParameterDateTimePickerControl,
  "[Dropdown](#cfn-quicksight-dashboard-parametercontrol-dropdown)" : ParameterDropDownControl,
  "[List](#cfn-quicksight-dashboard-parametercontrol-list)" : ParameterListControl,
  "[Slider](#cfn-quicksight-dashboard-parametercontrol-slider)" : ParameterSliderControl,
  "[TextArea](#cfn-quicksight-dashboard-parametercontrol-textarea)" : ParameterTextAreaControl,
  "[TextField](#cfn-quicksight-dashboard-parametercontrol-textfield)" : ParameterTextFieldControl
}
```

### YAML<a name="aws-properties-quicksight-dashboard-parametercontrol-syntax.yaml"></a>

```
  [DateTimePicker](#cfn-quicksight-dashboard-parametercontrol-datetimepicker): 
    ParameterDateTimePickerControl
  [Dropdown](#cfn-quicksight-dashboard-parametercontrol-dropdown): 
    ParameterDropDownControl
  [List](#cfn-quicksight-dashboard-parametercontrol-list): 
    ParameterListControl
  [Slider](#cfn-quicksight-dashboard-parametercontrol-slider): 
    ParameterSliderControl
  [TextArea](#cfn-quicksight-dashboard-parametercontrol-textarea): 
    ParameterTextAreaControl
  [TextField](#cfn-quicksight-dashboard-parametercontrol-textfield): 
    ParameterTextFieldControl
```

## Properties<a name="aws-properties-quicksight-dashboard-parametercontrol-properties"></a>

`DateTimePicker`  <a name="cfn-quicksight-dashboard-parametercontrol-datetimepicker"></a>
A control from a date parameter that specifies date and time\.  
*Required*: No  
*Type*: [ParameterDateTimePickerControl](aws-properties-quicksight-dashboard-parameterdatetimepickercontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dropdown`  <a name="cfn-quicksight-dashboard-parametercontrol-dropdown"></a>
A control to display a dropdown list with buttons that are used to select a single value\.  
*Required*: No  
*Type*: [ParameterDropDownControl](aws-properties-quicksight-dashboard-parameterdropdowncontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`List`  <a name="cfn-quicksight-dashboard-parametercontrol-list"></a>
A control to display a list with buttons or boxes that are used to select either a single value or multiple values\.  
*Required*: No  
*Type*: [ParameterListControl](aws-properties-quicksight-dashboard-parameterlistcontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slider`  <a name="cfn-quicksight-dashboard-parametercontrol-slider"></a>
A control to display a horizontal toggle bar\. This is used to change a value by sliding the toggle\.  
*Required*: No  
*Type*: [ParameterSliderControl](aws-properties-quicksight-dashboard-parameterslidercontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextArea`  <a name="cfn-quicksight-dashboard-parametercontrol-textarea"></a>
A control to display a text box that is used to enter multiple entries\.  
*Required*: No  
*Type*: [ParameterTextAreaControl](aws-properties-quicksight-dashboard-parametertextareacontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextField`  <a name="cfn-quicksight-dashboard-parametercontrol-textfield"></a>
A control to display a text box that is used to enter a single entry\.  
*Required*: No  
*Type*: [ParameterTextFieldControl](aws-properties-quicksight-dashboard-parametertextfieldcontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)