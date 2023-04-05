# AWS::QuickSight::Template TextFieldControlDisplayOptions<a name="aws-properties-quicksight-template-textfieldcontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-template-textfieldcontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-textfieldcontroldisplayoptions-syntax.json"></a>

```
{
  "[PlaceholderOptions](#cfn-quicksight-template-textfieldcontroldisplayoptions-placeholderoptions)" : TextControlPlaceholderOptions,
  "[TitleOptions](#cfn-quicksight-template-textfieldcontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-template-textfieldcontroldisplayoptions-syntax.yaml"></a>

```
  [PlaceholderOptions](#cfn-quicksight-template-textfieldcontroldisplayoptions-placeholderoptions): 
    TextControlPlaceholderOptions
  [TitleOptions](#cfn-quicksight-template-textfieldcontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-template-textfieldcontroldisplayoptions-properties"></a>

`PlaceholderOptions`  <a name="cfn-quicksight-template-textfieldcontroldisplayoptions-placeholderoptions"></a>
The configuration of the placeholder options in a text field control\.  
*Required*: No  
*Type*: [TextControlPlaceholderOptions](aws-properties-quicksight-template-textcontrolplaceholderoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-template-textfieldcontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-template-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)