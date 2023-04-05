# AWS::QuickSight::Dashboard ParameterTextAreaControl<a name="aws-properties-quicksight-dashboard-parametertextareacontrol"></a>

A control to display a text box that is used to enter multiple entries\.

## Syntax<a name="aws-properties-quicksight-dashboard-parametertextareacontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-parametertextareacontrol-syntax.json"></a>

```
{
  "[Delimiter](#cfn-quicksight-dashboard-parametertextareacontrol-delimiter)" : String,
  "[DisplayOptions](#cfn-quicksight-dashboard-parametertextareacontrol-displayoptions)" : TextAreaControlDisplayOptions,
  "[ParameterControlId](#cfn-quicksight-dashboard-parametertextareacontrol-parametercontrolid)" : String,
  "[SourceParameterName](#cfn-quicksight-dashboard-parametertextareacontrol-sourceparametername)" : String,
  "[Title](#cfn-quicksight-dashboard-parametertextareacontrol-title)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-parametertextareacontrol-syntax.yaml"></a>

```
  [Delimiter](#cfn-quicksight-dashboard-parametertextareacontrol-delimiter): String
  [DisplayOptions](#cfn-quicksight-dashboard-parametertextareacontrol-displayoptions): 
    TextAreaControlDisplayOptions
  [ParameterControlId](#cfn-quicksight-dashboard-parametertextareacontrol-parametercontrolid): String
  [SourceParameterName](#cfn-quicksight-dashboard-parametertextareacontrol-sourceparametername): String
  [Title](#cfn-quicksight-dashboard-parametertextareacontrol-title): String
```

## Properties<a name="aws-properties-quicksight-dashboard-parametertextareacontrol-properties"></a>

`Delimiter`  <a name="cfn-quicksight-dashboard-parametertextareacontrol-delimiter"></a>
The delimiter that is used to separate the lines in text\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayOptions`  <a name="cfn-quicksight-dashboard-parametertextareacontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [TextAreaControlDisplayOptions](aws-properties-quicksight-dashboard-textareacontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterControlId`  <a name="cfn-quicksight-dashboard-parametertextareacontrol-parametercontrolid"></a>
The ID of the `ParameterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceParameterName`  <a name="cfn-quicksight-dashboard-parametertextareacontrol-sourceparametername"></a>
The source parameter name of the `ParameterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-parametertextareacontrol-title"></a>
The title of the `ParameterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)