# AWS::QuickSight::Template ParameterTextFieldControl<a name="aws-properties-quicksight-template-parametertextfieldcontrol"></a>

A control to display a text box that is used to enter a single entry\.

## Syntax<a name="aws-properties-quicksight-template-parametertextfieldcontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-parametertextfieldcontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-template-parametertextfieldcontrol-displayoptions)" : TextFieldControlDisplayOptions,
  "[ParameterControlId](#cfn-quicksight-template-parametertextfieldcontrol-parametercontrolid)" : String,
  "[SourceParameterName](#cfn-quicksight-template-parametertextfieldcontrol-sourceparametername)" : String,
  "[Title](#cfn-quicksight-template-parametertextfieldcontrol-title)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-parametertextfieldcontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-template-parametertextfieldcontrol-displayoptions): 
    TextFieldControlDisplayOptions
  [ParameterControlId](#cfn-quicksight-template-parametertextfieldcontrol-parametercontrolid): String
  [SourceParameterName](#cfn-quicksight-template-parametertextfieldcontrol-sourceparametername): String
  [Title](#cfn-quicksight-template-parametertextfieldcontrol-title): String
```

## Properties<a name="aws-properties-quicksight-template-parametertextfieldcontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-template-parametertextfieldcontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [TextFieldControlDisplayOptions](aws-properties-quicksight-template-textfieldcontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterControlId`  <a name="cfn-quicksight-template-parametertextfieldcontrol-parametercontrolid"></a>
The ID of the `ParameterTextFieldControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceParameterName`  <a name="cfn-quicksight-template-parametertextfieldcontrol-sourceparametername"></a>
The source parameter name of the `ParameterTextFieldControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-parametertextfieldcontrol-title"></a>
The title of the `ParameterTextFieldControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)