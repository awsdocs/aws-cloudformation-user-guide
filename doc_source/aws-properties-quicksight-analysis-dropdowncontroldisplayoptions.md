# AWS::QuickSight::Analysis DropDownControlDisplayOptions<a name="aws-properties-quicksight-analysis-dropdowncontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-analysis-dropdowncontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-dropdowncontroldisplayoptions-syntax.json"></a>

```
{
  "[SelectAllOptions](#cfn-quicksight-analysis-dropdowncontroldisplayoptions-selectalloptions)" : ListControlSelectAllOptions,
  "[TitleOptions](#cfn-quicksight-analysis-dropdowncontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-dropdowncontroldisplayoptions-syntax.yaml"></a>

```
  [SelectAllOptions](#cfn-quicksight-analysis-dropdowncontroldisplayoptions-selectalloptions): 
    ListControlSelectAllOptions
  [TitleOptions](#cfn-quicksight-analysis-dropdowncontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-dropdowncontroldisplayoptions-properties"></a>

`SelectAllOptions`  <a name="cfn-quicksight-analysis-dropdowncontroldisplayoptions-selectalloptions"></a>
The configuration of the `Select all` options in a dropdown control\.  
*Required*: No  
*Type*: [ListControlSelectAllOptions](aws-properties-quicksight-analysis-listcontrolselectalloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-analysis-dropdowncontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-analysis-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)