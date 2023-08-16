# AWS::QuickSight::Template FilterTextAreaControl<a name="aws-properties-quicksight-template-filtertextareacontrol"></a>

A control to display a text box that is used to enter multiple entries\.

## Syntax<a name="aws-properties-quicksight-template-filtertextareacontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filtertextareacontrol-syntax.json"></a>

```
{
  "[Delimiter](#cfn-quicksight-template-filtertextareacontrol-delimiter)" : String,
  "[DisplayOptions](#cfn-quicksight-template-filtertextareacontrol-displayoptions)" : TextAreaControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-template-filtertextareacontrol-filtercontrolid)" : String,
  "[SourceFilterId](#cfn-quicksight-template-filtertextareacontrol-sourcefilterid)" : String,
  "[Title](#cfn-quicksight-template-filtertextareacontrol-title)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-filtertextareacontrol-syntax.yaml"></a>

```
  [Delimiter](#cfn-quicksight-template-filtertextareacontrol-delimiter): String
  [DisplayOptions](#cfn-quicksight-template-filtertextareacontrol-displayoptions): 
    TextAreaControlDisplayOptions
  [FilterControlId](#cfn-quicksight-template-filtertextareacontrol-filtercontrolid): String
  [SourceFilterId](#cfn-quicksight-template-filtertextareacontrol-sourcefilterid): String
  [Title](#cfn-quicksight-template-filtertextareacontrol-title): String
```

## Properties<a name="aws-properties-quicksight-template-filtertextareacontrol-properties"></a>

`Delimiter`  <a name="cfn-quicksight-template-filtertextareacontrol-delimiter"></a>
The delimiter that is used to separate the lines in text\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayOptions`  <a name="cfn-quicksight-template-filtertextareacontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [TextAreaControlDisplayOptions](aws-properties-quicksight-template-textareacontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-template-filtertextareacontrol-filtercontrolid"></a>
The ID of the `FilterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-template-filtertextareacontrol-sourcefilterid"></a>
The source filter ID of the `FilterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-filtertextareacontrol-title"></a>
The title of the `FilterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)