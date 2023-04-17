# AWS::QuickSight::Analysis TextFieldControlDisplayOptions<a name="aws-properties-quicksight-analysis-textfieldcontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-analysis-textfieldcontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-textfieldcontroldisplayoptions-syntax.json"></a>

```
{
  "[PlaceholderOptions](#cfn-quicksight-analysis-textfieldcontroldisplayoptions-placeholderoptions)" : TextControlPlaceholderOptions,
  "[TitleOptions](#cfn-quicksight-analysis-textfieldcontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-textfieldcontroldisplayoptions-syntax.yaml"></a>

```
  [PlaceholderOptions](#cfn-quicksight-analysis-textfieldcontroldisplayoptions-placeholderoptions): 
    TextControlPlaceholderOptions
  [TitleOptions](#cfn-quicksight-analysis-textfieldcontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-textfieldcontroldisplayoptions-properties"></a>

`PlaceholderOptions`  <a name="cfn-quicksight-analysis-textfieldcontroldisplayoptions-placeholderoptions"></a>
The configuration of the placeholder options in a text field control\.  
*Required*: No  
*Type*: [TextControlPlaceholderOptions](aws-properties-quicksight-analysis-textcontrolplaceholderoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-analysis-textfieldcontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-analysis-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)