# AWS::QuickSight::Analysis KPIConditionalFormattingOption<a name="aws-properties-quicksight-analysis-kpiconditionalformattingoption"></a>

The conditional formatting options of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-analysis-kpiconditionalformattingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-kpiconditionalformattingoption-syntax.json"></a>

```
{
  "[PrimaryValue](#cfn-quicksight-analysis-kpiconditionalformattingoption-primaryvalue)" : KPIPrimaryValueConditionalFormatting,
  "[ProgressBar](#cfn-quicksight-analysis-kpiconditionalformattingoption-progressbar)" : KPIProgressBarConditionalFormatting
}
```

### YAML<a name="aws-properties-quicksight-analysis-kpiconditionalformattingoption-syntax.yaml"></a>

```
  [PrimaryValue](#cfn-quicksight-analysis-kpiconditionalformattingoption-primaryvalue): 
    KPIPrimaryValueConditionalFormatting
  [ProgressBar](#cfn-quicksight-analysis-kpiconditionalformattingoption-progressbar): 
    KPIProgressBarConditionalFormatting
```

## Properties<a name="aws-properties-quicksight-analysis-kpiconditionalformattingoption-properties"></a>

`PrimaryValue`  <a name="cfn-quicksight-analysis-kpiconditionalformattingoption-primaryvalue"></a>
The conditional formatting for the primary value of a KPI visual\.  
*Required*: No  
*Type*: [KPIPrimaryValueConditionalFormatting](aws-properties-quicksight-analysis-kpiprimaryvalueconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgressBar`  <a name="cfn-quicksight-analysis-kpiconditionalformattingoption-progressbar"></a>
The conditional formatting for the progress bar of a KPI visual\.  
*Required*: No  
*Type*: [KPIProgressBarConditionalFormatting](aws-properties-quicksight-analysis-kpiprogressbarconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)