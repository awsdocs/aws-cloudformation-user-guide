# AWS::QuickSight::Template FilterTextFieldControl<a name="aws-properties-quicksight-template-filtertextfieldcontrol"></a>

A control to display a text box that is used to enter a single entry\.

## Syntax<a name="aws-properties-quicksight-template-filtertextfieldcontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filtertextfieldcontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-template-filtertextfieldcontrol-displayoptions)" : TextFieldControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-template-filtertextfieldcontrol-filtercontrolid)" : String,
  "[SourceFilterId](#cfn-quicksight-template-filtertextfieldcontrol-sourcefilterid)" : String,
  "[Title](#cfn-quicksight-template-filtertextfieldcontrol-title)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-filtertextfieldcontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-template-filtertextfieldcontrol-displayoptions): 
    TextFieldControlDisplayOptions
  [FilterControlId](#cfn-quicksight-template-filtertextfieldcontrol-filtercontrolid): String
  [SourceFilterId](#cfn-quicksight-template-filtertextfieldcontrol-sourcefilterid): String
  [Title](#cfn-quicksight-template-filtertextfieldcontrol-title): String
```

## Properties<a name="aws-properties-quicksight-template-filtertextfieldcontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-template-filtertextfieldcontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [TextFieldControlDisplayOptions](aws-properties-quicksight-template-textfieldcontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-template-filtertextfieldcontrol-filtercontrolid"></a>
The ID of the `FilterTextFieldControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-template-filtertextfieldcontrol-sourcefilterid"></a>
The source filter ID of the `FilterTextFieldControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-filtertextfieldcontrol-title"></a>
The title of the `FilterTextFieldControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)