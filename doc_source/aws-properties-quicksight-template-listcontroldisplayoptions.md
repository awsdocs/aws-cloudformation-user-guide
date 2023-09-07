# AWS::QuickSight::Template ListControlDisplayOptions<a name="aws-properties-quicksight-template-listcontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-template-listcontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-listcontroldisplayoptions-syntax.json"></a>

```
{
  "[InfoIconLabelOptions](#cfn-quicksight-template-listcontroldisplayoptions-infoiconlabeloptions)" : SheetControlInfoIconLabelOptions,
  "[SearchOptions](#cfn-quicksight-template-listcontroldisplayoptions-searchoptions)" : ListControlSearchOptions,
  "[SelectAllOptions](#cfn-quicksight-template-listcontroldisplayoptions-selectalloptions)" : ListControlSelectAllOptions,
  "[TitleOptions](#cfn-quicksight-template-listcontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-template-listcontroldisplayoptions-syntax.yaml"></a>

```
  [InfoIconLabelOptions](#cfn-quicksight-template-listcontroldisplayoptions-infoiconlabeloptions): 
    SheetControlInfoIconLabelOptions
  [SearchOptions](#cfn-quicksight-template-listcontroldisplayoptions-searchoptions): 
    ListControlSearchOptions
  [SelectAllOptions](#cfn-quicksight-template-listcontroldisplayoptions-selectalloptions): 
    ListControlSelectAllOptions
  [TitleOptions](#cfn-quicksight-template-listcontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-template-listcontroldisplayoptions-properties"></a>

`InfoIconLabelOptions`  <a name="cfn-quicksight-template-listcontroldisplayoptions-infoiconlabeloptions"></a>
The configuration of info icon label options\.  
*Required*: No  
*Type*: [SheetControlInfoIconLabelOptions](aws-properties-quicksight-template-sheetcontrolinfoiconlabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SearchOptions`  <a name="cfn-quicksight-template-listcontroldisplayoptions-searchoptions"></a>
The configuration of the search options in a list control\.  
*Required*: No  
*Type*: [ListControlSearchOptions](aws-properties-quicksight-template-listcontrolsearchoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectAllOptions`  <a name="cfn-quicksight-template-listcontroldisplayoptions-selectalloptions"></a>
The configuration of the `Select all` options in a list control\.  
*Required*: No  
*Type*: [ListControlSelectAllOptions](aws-properties-quicksight-template-listcontrolselectalloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-template-listcontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-template-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)