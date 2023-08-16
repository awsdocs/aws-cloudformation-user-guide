# AWS::QuickSight::Dashboard FilterListControl<a name="aws-properties-quicksight-dashboard-filterlistcontrol"></a>

A control to display a list of buttons or boxes\. This is used to select either a single value or multiple values\.

## Syntax<a name="aws-properties-quicksight-dashboard-filterlistcontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filterlistcontrol-syntax.json"></a>

```
{
  "[CascadingControlConfiguration](#cfn-quicksight-dashboard-filterlistcontrol-cascadingcontrolconfiguration)" : CascadingControlConfiguration,
  "[DisplayOptions](#cfn-quicksight-dashboard-filterlistcontrol-displayoptions)" : ListControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-dashboard-filterlistcontrol-filtercontrolid)" : String,
  "[SelectableValues](#cfn-quicksight-dashboard-filterlistcontrol-selectablevalues)" : FilterSelectableValues,
  "[SourceFilterId](#cfn-quicksight-dashboard-filterlistcontrol-sourcefilterid)" : String,
  "[Title](#cfn-quicksight-dashboard-filterlistcontrol-title)" : String,
  "[Type](#cfn-quicksight-dashboard-filterlistcontrol-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filterlistcontrol-syntax.yaml"></a>

```
  [CascadingControlConfiguration](#cfn-quicksight-dashboard-filterlistcontrol-cascadingcontrolconfiguration): 
    CascadingControlConfiguration
  [DisplayOptions](#cfn-quicksight-dashboard-filterlistcontrol-displayoptions): 
    ListControlDisplayOptions
  [FilterControlId](#cfn-quicksight-dashboard-filterlistcontrol-filtercontrolid): String
  [SelectableValues](#cfn-quicksight-dashboard-filterlistcontrol-selectablevalues): 
    FilterSelectableValues
  [SourceFilterId](#cfn-quicksight-dashboard-filterlistcontrol-sourcefilterid): String
  [Title](#cfn-quicksight-dashboard-filterlistcontrol-title): String
  [Type](#cfn-quicksight-dashboard-filterlistcontrol-type): String
```

## Properties<a name="aws-properties-quicksight-dashboard-filterlistcontrol-properties"></a>

`CascadingControlConfiguration`  <a name="cfn-quicksight-dashboard-filterlistcontrol-cascadingcontrolconfiguration"></a>
The values that are displayed in a control can be configured to only show values that are valid based on what's selected in other controls\.  
*Required*: No  
*Type*: [CascadingControlConfiguration](aws-properties-quicksight-dashboard-cascadingcontrolconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayOptions`  <a name="cfn-quicksight-dashboard-filterlistcontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [ListControlDisplayOptions](aws-properties-quicksight-dashboard-listcontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-dashboard-filterlistcontrol-filtercontrolid"></a>
The ID of the `FilterListControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectableValues`  <a name="cfn-quicksight-dashboard-filterlistcontrol-selectablevalues"></a>
A list of selectable values that are used in a control\.  
*Required*: No  
*Type*: [FilterSelectableValues](aws-properties-quicksight-dashboard-filterselectablevalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-dashboard-filterlistcontrol-sourcefilterid"></a>
The source filter ID of the `FilterListControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-filterlistcontrol-title"></a>
The title of the `FilterListControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-filterlistcontrol-type"></a>
The type of `FilterListControl`\. Choose one of the following options:  
+  `MULTI_SELECT`: The user can select multiple entries from the list\.
+  `SINGLE_SELECT`: The user can select a single entry from the list\.
*Required*: No  
*Type*: String  
*Allowed values*: `MULTI_SELECT | SINGLE_SELECT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)