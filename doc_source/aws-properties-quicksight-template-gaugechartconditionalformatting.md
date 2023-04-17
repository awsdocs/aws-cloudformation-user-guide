# AWS::QuickSight::Template GaugeChartConditionalFormatting<a name="aws-properties-quicksight-template-gaugechartconditionalformatting"></a>

The conditional formatting of a `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-template-gaugechartconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-gaugechartconditionalformatting-syntax.json"></a>

```
{
  "[ConditionalFormattingOptions](#cfn-quicksight-template-gaugechartconditionalformatting-conditionalformattingoptions)" : [ GaugeChartConditionalFormattingOption, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-gaugechartconditionalformatting-syntax.yaml"></a>

```
  [ConditionalFormattingOptions](#cfn-quicksight-template-gaugechartconditionalformatting-conditionalformattingoptions): 
    - GaugeChartConditionalFormattingOption
```

## Properties<a name="aws-properties-quicksight-template-gaugechartconditionalformatting-properties"></a>

`ConditionalFormattingOptions`  <a name="cfn-quicksight-template-gaugechartconditionalformatting-conditionalformattingoptions"></a>
Conditional formatting options of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: List of [GaugeChartConditionalFormattingOption](aws-properties-quicksight-template-gaugechartconditionalformattingoption.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)