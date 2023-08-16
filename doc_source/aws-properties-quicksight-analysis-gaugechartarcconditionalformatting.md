# AWS::QuickSight::Analysis GaugeChartArcConditionalFormatting<a name="aws-properties-quicksight-analysis-gaugechartarcconditionalformatting"></a>

The options that determine the presentation of the arc of a `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-gaugechartarcconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-gaugechartarcconditionalformatting-syntax.json"></a>

```
{
  "[ForegroundColor](#cfn-quicksight-analysis-gaugechartarcconditionalformatting-foregroundcolor)" : ConditionalFormattingColor
}
```

### YAML<a name="aws-properties-quicksight-analysis-gaugechartarcconditionalformatting-syntax.yaml"></a>

```
  [ForegroundColor](#cfn-quicksight-analysis-gaugechartarcconditionalformatting-foregroundcolor): 
    ConditionalFormattingColor
```

## Properties<a name="aws-properties-quicksight-analysis-gaugechartarcconditionalformatting-properties"></a>

`ForegroundColor`  <a name="cfn-quicksight-analysis-gaugechartarcconditionalformatting-foregroundcolor"></a>
The conditional formatting of the arc foreground color\.  
*Required*: No  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-analysis-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)