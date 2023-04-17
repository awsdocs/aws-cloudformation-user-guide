# AWS::QuickSight::Template KPIConditionalFormatting<a name="aws-properties-quicksight-template-kpiconditionalformatting"></a>

The conditional formatting of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-template-kpiconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-kpiconditionalformatting-syntax.json"></a>

```
{
  "[ConditionalFormattingOptions](#cfn-quicksight-template-kpiconditionalformatting-conditionalformattingoptions)" : [ KPIConditionalFormattingOption, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-kpiconditionalformatting-syntax.yaml"></a>

```
  [ConditionalFormattingOptions](#cfn-quicksight-template-kpiconditionalformatting-conditionalformattingoptions): 
    - KPIConditionalFormattingOption
```

## Properties<a name="aws-properties-quicksight-template-kpiconditionalformatting-properties"></a>

`ConditionalFormattingOptions`  <a name="cfn-quicksight-template-kpiconditionalformatting-conditionalformattingoptions"></a>
The conditional formatting options of a KPI visual\.  
*Required*: No  
*Type*: List of [KPIConditionalFormattingOption](aws-properties-quicksight-template-kpiconditionalformattingoption.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)