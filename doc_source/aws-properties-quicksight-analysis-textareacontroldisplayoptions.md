# AWS::QuickSight::Analysis TextAreaControlDisplayOptions<a name="aws-properties-quicksight-analysis-textareacontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-analysis-textareacontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-textareacontroldisplayoptions-syntax.json"></a>

```
{
  "[PlaceholderOptions](#cfn-quicksight-analysis-textareacontroldisplayoptions-placeholderoptions)" : TextControlPlaceholderOptions,
  "[TitleOptions](#cfn-quicksight-analysis-textareacontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-textareacontroldisplayoptions-syntax.yaml"></a>

```
  [PlaceholderOptions](#cfn-quicksight-analysis-textareacontroldisplayoptions-placeholderoptions): 
    TextControlPlaceholderOptions
  [TitleOptions](#cfn-quicksight-analysis-textareacontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-textareacontroldisplayoptions-properties"></a>

`PlaceholderOptions`  <a name="cfn-quicksight-analysis-textareacontroldisplayoptions-placeholderoptions"></a>
The configuration of the placeholder options in a text area control\.  
*Required*: No  
*Type*: [TextControlPlaceholderOptions](aws-properties-quicksight-analysis-textcontrolplaceholderoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-analysis-textareacontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-analysis-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)