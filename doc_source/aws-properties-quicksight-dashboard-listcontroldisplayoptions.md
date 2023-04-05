# AWS::QuickSight::Dashboard ListControlDisplayOptions<a name="aws-properties-quicksight-dashboard-listcontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-dashboard-listcontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-listcontroldisplayoptions-syntax.json"></a>

```
{
  "[SearchOptions](#cfn-quicksight-dashboard-listcontroldisplayoptions-searchoptions)" : ListControlSearchOptions,
  "[SelectAllOptions](#cfn-quicksight-dashboard-listcontroldisplayoptions-selectalloptions)" : ListControlSelectAllOptions,
  "[TitleOptions](#cfn-quicksight-dashboard-listcontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-dashboard-listcontroldisplayoptions-syntax.yaml"></a>

```
  [SearchOptions](#cfn-quicksight-dashboard-listcontroldisplayoptions-searchoptions): 
    ListControlSearchOptions
  [SelectAllOptions](#cfn-quicksight-dashboard-listcontroldisplayoptions-selectalloptions): 
    ListControlSelectAllOptions
  [TitleOptions](#cfn-quicksight-dashboard-listcontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-dashboard-listcontroldisplayoptions-properties"></a>

`SearchOptions`  <a name="cfn-quicksight-dashboard-listcontroldisplayoptions-searchoptions"></a>
The configuration of the search options in a list control\.  
*Required*: No  
*Type*: [ListControlSearchOptions](aws-properties-quicksight-dashboard-listcontrolsearchoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectAllOptions`  <a name="cfn-quicksight-dashboard-listcontroldisplayoptions-selectalloptions"></a>
The configuration of the `Select all` options in a list control\.  
*Required*: No  
*Type*: [ListControlSelectAllOptions](aws-properties-quicksight-dashboard-listcontrolselectalloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-dashboard-listcontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-dashboard-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)