# AWS::QuickSight::Template TextAreaControlDisplayOptions<a name="aws-properties-quicksight-template-textareacontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-template-textareacontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-textareacontroldisplayoptions-syntax.json"></a>

```
{
  "[InfoIconLabelOptions](#cfn-quicksight-template-textareacontroldisplayoptions-infoiconlabeloptions)" : SheetControlInfoIconLabelOptions,
  "[PlaceholderOptions](#cfn-quicksight-template-textareacontroldisplayoptions-placeholderoptions)" : TextControlPlaceholderOptions,
  "[TitleOptions](#cfn-quicksight-template-textareacontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-template-textareacontroldisplayoptions-syntax.yaml"></a>

```
  [InfoIconLabelOptions](#cfn-quicksight-template-textareacontroldisplayoptions-infoiconlabeloptions): 
    SheetControlInfoIconLabelOptions
  [PlaceholderOptions](#cfn-quicksight-template-textareacontroldisplayoptions-placeholderoptions): 
    TextControlPlaceholderOptions
  [TitleOptions](#cfn-quicksight-template-textareacontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-template-textareacontroldisplayoptions-properties"></a>

`InfoIconLabelOptions`  <a name="cfn-quicksight-template-textareacontroldisplayoptions-infoiconlabeloptions"></a>
The configuration of info icon label options\.  
*Required*: No  
*Type*: [SheetControlInfoIconLabelOptions](aws-properties-quicksight-template-sheetcontrolinfoiconlabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlaceholderOptions`  <a name="cfn-quicksight-template-textareacontroldisplayoptions-placeholderoptions"></a>
The configuration of the placeholder options in a text area control\.  
*Required*: No  
*Type*: [TextControlPlaceholderOptions](aws-properties-quicksight-template-textcontrolplaceholderoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-template-textareacontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-template-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)