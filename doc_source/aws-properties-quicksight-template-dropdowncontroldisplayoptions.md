# AWS::QuickSight::Template DropDownControlDisplayOptions<a name="aws-properties-quicksight-template-dropdowncontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-template-dropdowncontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-dropdowncontroldisplayoptions-syntax.json"></a>

```
{
  "[InfoIconLabelOptions](#cfn-quicksight-template-dropdowncontroldisplayoptions-infoiconlabeloptions)" : SheetControlInfoIconLabelOptions,
  "[SelectAllOptions](#cfn-quicksight-template-dropdowncontroldisplayoptions-selectalloptions)" : ListControlSelectAllOptions,
  "[TitleOptions](#cfn-quicksight-template-dropdowncontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-template-dropdowncontroldisplayoptions-syntax.yaml"></a>

```
  [InfoIconLabelOptions](#cfn-quicksight-template-dropdowncontroldisplayoptions-infoiconlabeloptions): 
    SheetControlInfoIconLabelOptions
  [SelectAllOptions](#cfn-quicksight-template-dropdowncontroldisplayoptions-selectalloptions): 
    ListControlSelectAllOptions
  [TitleOptions](#cfn-quicksight-template-dropdowncontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-template-dropdowncontroldisplayoptions-properties"></a>

`InfoIconLabelOptions`  <a name="cfn-quicksight-template-dropdowncontroldisplayoptions-infoiconlabeloptions"></a>
The configuration of info icon label options\.  
*Required*: No  
*Type*: [SheetControlInfoIconLabelOptions](aws-properties-quicksight-template-sheetcontrolinfoiconlabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectAllOptions`  <a name="cfn-quicksight-template-dropdowncontroldisplayoptions-selectalloptions"></a>
The configuration of the `Select all` options in a dropdown control\.  
*Required*: No  
*Type*: [ListControlSelectAllOptions](aws-properties-quicksight-template-listcontrolselectalloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-template-dropdowncontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-template-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)