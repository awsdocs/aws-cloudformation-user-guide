# AWS::QuickSight::Dashboard KPIPrimaryValueConditionalFormatting<a name="aws-properties-quicksight-dashboard-kpiprimaryvalueconditionalformatting"></a>

The conditional formatting for the primary value of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-kpiprimaryvalueconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-kpiprimaryvalueconditionalformatting-syntax.json"></a>

```
{
  "[Icon](#cfn-quicksight-dashboard-kpiprimaryvalueconditionalformatting-icon)" : ConditionalFormattingIcon,
  "[TextColor](#cfn-quicksight-dashboard-kpiprimaryvalueconditionalformatting-textcolor)" : ConditionalFormattingColor
}
```

### YAML<a name="aws-properties-quicksight-dashboard-kpiprimaryvalueconditionalformatting-syntax.yaml"></a>

```
  [Icon](#cfn-quicksight-dashboard-kpiprimaryvalueconditionalformatting-icon): 
    ConditionalFormattingIcon
  [TextColor](#cfn-quicksight-dashboard-kpiprimaryvalueconditionalformatting-textcolor): 
    ConditionalFormattingColor
```

## Properties<a name="aws-properties-quicksight-dashboard-kpiprimaryvalueconditionalformatting-properties"></a>

`Icon`  <a name="cfn-quicksight-dashboard-kpiprimaryvalueconditionalformatting-icon"></a>
The conditional formatting of the primary value's icon\.  
*Required*: No  
*Type*: [ConditionalFormattingIcon](aws-properties-quicksight-dashboard-conditionalformattingicon.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextColor`  <a name="cfn-quicksight-dashboard-kpiprimaryvalueconditionalformatting-textcolor"></a>
The conditional formatting of the primary value's text color\.  
*Required*: No  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-dashboard-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)