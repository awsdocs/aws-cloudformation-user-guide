# AWS::QuickSight::Analysis KPIPrimaryValueConditionalFormatting<a name="aws-properties-quicksight-analysis-kpiprimaryvalueconditionalformatting"></a>

The conditional formatting for the primary value of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-analysis-kpiprimaryvalueconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-kpiprimaryvalueconditionalformatting-syntax.json"></a>

```
{
  "[Icon](#cfn-quicksight-analysis-kpiprimaryvalueconditionalformatting-icon)" : ConditionalFormattingIcon,
  "[TextColor](#cfn-quicksight-analysis-kpiprimaryvalueconditionalformatting-textcolor)" : ConditionalFormattingColor
}
```

### YAML<a name="aws-properties-quicksight-analysis-kpiprimaryvalueconditionalformatting-syntax.yaml"></a>

```
  [Icon](#cfn-quicksight-analysis-kpiprimaryvalueconditionalformatting-icon): 
    ConditionalFormattingIcon
  [TextColor](#cfn-quicksight-analysis-kpiprimaryvalueconditionalformatting-textcolor): 
    ConditionalFormattingColor
```

## Properties<a name="aws-properties-quicksight-analysis-kpiprimaryvalueconditionalformatting-properties"></a>

`Icon`  <a name="cfn-quicksight-analysis-kpiprimaryvalueconditionalformatting-icon"></a>
The conditional formatting of the primary value's icon\.  
*Required*: No  
*Type*: [ConditionalFormattingIcon](aws-properties-quicksight-analysis-conditionalformattingicon.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextColor`  <a name="cfn-quicksight-analysis-kpiprimaryvalueconditionalformatting-textcolor"></a>
The conditional formatting of the primary value's text color\.  
*Required*: No  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-analysis-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)