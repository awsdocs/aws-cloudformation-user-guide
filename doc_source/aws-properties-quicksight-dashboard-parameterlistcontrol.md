# AWS::QuickSight::Dashboard ParameterListControl<a name="aws-properties-quicksight-dashboard-parameterlistcontrol"></a>

A control to display a list with buttons or boxes that are used to select either a single value or multiple values\.

## Syntax<a name="aws-properties-quicksight-dashboard-parameterlistcontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-parameterlistcontrol-syntax.json"></a>

```
{
  "[CascadingControlConfiguration](#cfn-quicksight-dashboard-parameterlistcontrol-cascadingcontrolconfiguration)" : CascadingControlConfiguration,
  "[DisplayOptions](#cfn-quicksight-dashboard-parameterlistcontrol-displayoptions)" : ListControlDisplayOptions,
  "[ParameterControlId](#cfn-quicksight-dashboard-parameterlistcontrol-parametercontrolid)" : String,
  "[SelectableValues](#cfn-quicksight-dashboard-parameterlistcontrol-selectablevalues)" : ParameterSelectableValues,
  "[SourceParameterName](#cfn-quicksight-dashboard-parameterlistcontrol-sourceparametername)" : String,
  "[Title](#cfn-quicksight-dashboard-parameterlistcontrol-title)" : String,
  "[Type](#cfn-quicksight-dashboard-parameterlistcontrol-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-parameterlistcontrol-syntax.yaml"></a>

```
  [CascadingControlConfiguration](#cfn-quicksight-dashboard-parameterlistcontrol-cascadingcontrolconfiguration): 
    CascadingControlConfiguration
  [DisplayOptions](#cfn-quicksight-dashboard-parameterlistcontrol-displayoptions): 
    ListControlDisplayOptions
  [ParameterControlId](#cfn-quicksight-dashboard-parameterlistcontrol-parametercontrolid): String
  [SelectableValues](#cfn-quicksight-dashboard-parameterlistcontrol-selectablevalues): 
    ParameterSelectableValues
  [SourceParameterName](#cfn-quicksight-dashboard-parameterlistcontrol-sourceparametername): String
  [Title](#cfn-quicksight-dashboard-parameterlistcontrol-title): String
  [Type](#cfn-quicksight-dashboard-parameterlistcontrol-type): String
```

## Properties<a name="aws-properties-quicksight-dashboard-parameterlistcontrol-properties"></a>

`CascadingControlConfiguration`  <a name="cfn-quicksight-dashboard-parameterlistcontrol-cascadingcontrolconfiguration"></a>
The values that are displayed in a control can be configured to only show values that are valid based on what's selected in other controls\.  
*Required*: No  
*Type*: [CascadingControlConfiguration](aws-properties-quicksight-dashboard-cascadingcontrolconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayOptions`  <a name="cfn-quicksight-dashboard-parameterlistcontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [ListControlDisplayOptions](aws-properties-quicksight-dashboard-listcontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterControlId`  <a name="cfn-quicksight-dashboard-parameterlistcontrol-parametercontrolid"></a>
The ID of the `ParameterListControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectableValues`  <a name="cfn-quicksight-dashboard-parameterlistcontrol-selectablevalues"></a>
A list of selectable values that are used in a control\.  
*Required*: No  
*Type*: [ParameterSelectableValues](aws-properties-quicksight-dashboard-parameterselectablevalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceParameterName`  <a name="cfn-quicksight-dashboard-parameterlistcontrol-sourceparametername"></a>
The source parameter name of the `ParameterListControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-parameterlistcontrol-title"></a>
The title of the `ParameterListControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-parameterlistcontrol-type"></a>
The type of `ParameterListControl`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `MULTI_SELECT | SINGLE_SELECT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)