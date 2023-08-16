# AWS::QuickSight::Dashboard ParameterDropDownControl<a name="aws-properties-quicksight-dashboard-parameterdropdowncontrol"></a>

A control to display a dropdown list with buttons that are used to select a single value\.

## Syntax<a name="aws-properties-quicksight-dashboard-parameterdropdowncontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-parameterdropdowncontrol-syntax.json"></a>

```
{
  "[CascadingControlConfiguration](#cfn-quicksight-dashboard-parameterdropdowncontrol-cascadingcontrolconfiguration)" : CascadingControlConfiguration,
  "[DisplayOptions](#cfn-quicksight-dashboard-parameterdropdowncontrol-displayoptions)" : DropDownControlDisplayOptions,
  "[ParameterControlId](#cfn-quicksight-dashboard-parameterdropdowncontrol-parametercontrolid)" : String,
  "[SelectableValues](#cfn-quicksight-dashboard-parameterdropdowncontrol-selectablevalues)" : ParameterSelectableValues,
  "[SourceParameterName](#cfn-quicksight-dashboard-parameterdropdowncontrol-sourceparametername)" : String,
  "[Title](#cfn-quicksight-dashboard-parameterdropdowncontrol-title)" : String,
  "[Type](#cfn-quicksight-dashboard-parameterdropdowncontrol-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-parameterdropdowncontrol-syntax.yaml"></a>

```
  [CascadingControlConfiguration](#cfn-quicksight-dashboard-parameterdropdowncontrol-cascadingcontrolconfiguration): 
    CascadingControlConfiguration
  [DisplayOptions](#cfn-quicksight-dashboard-parameterdropdowncontrol-displayoptions): 
    DropDownControlDisplayOptions
  [ParameterControlId](#cfn-quicksight-dashboard-parameterdropdowncontrol-parametercontrolid): String
  [SelectableValues](#cfn-quicksight-dashboard-parameterdropdowncontrol-selectablevalues): 
    ParameterSelectableValues
  [SourceParameterName](#cfn-quicksight-dashboard-parameterdropdowncontrol-sourceparametername): String
  [Title](#cfn-quicksight-dashboard-parameterdropdowncontrol-title): String
  [Type](#cfn-quicksight-dashboard-parameterdropdowncontrol-type): String
```

## Properties<a name="aws-properties-quicksight-dashboard-parameterdropdowncontrol-properties"></a>

`CascadingControlConfiguration`  <a name="cfn-quicksight-dashboard-parameterdropdowncontrol-cascadingcontrolconfiguration"></a>
The values that are displayed in a control can be configured to only show values that are valid based on what's selected in other controls\.  
*Required*: No  
*Type*: [CascadingControlConfiguration](aws-properties-quicksight-dashboard-cascadingcontrolconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayOptions`  <a name="cfn-quicksight-dashboard-parameterdropdowncontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [DropDownControlDisplayOptions](aws-properties-quicksight-dashboard-dropdowncontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterControlId`  <a name="cfn-quicksight-dashboard-parameterdropdowncontrol-parametercontrolid"></a>
The ID of the `ParameterDropDownControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectableValues`  <a name="cfn-quicksight-dashboard-parameterdropdowncontrol-selectablevalues"></a>
A list of selectable values that are used in a control\.  
*Required*: No  
*Type*: [ParameterSelectableValues](aws-properties-quicksight-dashboard-parameterselectablevalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceParameterName`  <a name="cfn-quicksight-dashboard-parameterdropdowncontrol-sourceparametername"></a>
The source parameter name of the `ParameterDropDownControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-parameterdropdowncontrol-title"></a>
The title of the `ParameterDropDownControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-parameterdropdowncontrol-type"></a>
The type parameter name of the `ParameterDropDownControl`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `MULTI_SELECT | SINGLE_SELECT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)