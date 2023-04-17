# AWS::QuickSight::Analysis GaugeChartConditionalFormattingOption<a name="aws-properties-quicksight-analysis-gaugechartconditionalformattingoption"></a>

Conditional formatting options of a `GaugeChartVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-gaugechartconditionalformattingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-gaugechartconditionalformattingoption-syntax.json"></a>

```
{
  "[Arc](#cfn-quicksight-analysis-gaugechartconditionalformattingoption-arc)" : GaugeChartArcConditionalFormatting,
  "[PrimaryValue](#cfn-quicksight-analysis-gaugechartconditionalformattingoption-primaryvalue)" : GaugeChartPrimaryValueConditionalFormatting
}
```

### YAML<a name="aws-properties-quicksight-analysis-gaugechartconditionalformattingoption-syntax.yaml"></a>

```
  [Arc](#cfn-quicksight-analysis-gaugechartconditionalformattingoption-arc): 
    GaugeChartArcConditionalFormatting
  [PrimaryValue](#cfn-quicksight-analysis-gaugechartconditionalformattingoption-primaryvalue): 
    GaugeChartPrimaryValueConditionalFormatting
```

## Properties<a name="aws-properties-quicksight-analysis-gaugechartconditionalformattingoption-properties"></a>

`Arc`  <a name="cfn-quicksight-analysis-gaugechartconditionalformattingoption-arc"></a>
The options that determine the presentation of the arc of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [GaugeChartArcConditionalFormatting](aws-properties-quicksight-analysis-gaugechartarcconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrimaryValue`  <a name="cfn-quicksight-analysis-gaugechartconditionalformattingoption-primaryvalue"></a>
The conditional formatting for the primary value of a `GaugeChartVisual`\.  
*Required*: No  
*Type*: [GaugeChartPrimaryValueConditionalFormatting](aws-properties-quicksight-analysis-gaugechartprimaryvalueconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)