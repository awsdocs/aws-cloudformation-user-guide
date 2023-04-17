# AWS::QuickSight::Dashboard KPIConditionalFormattingOption<a name="aws-properties-quicksight-dashboard-kpiconditionalformattingoption"></a>

The conditional formatting options of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-kpiconditionalformattingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-kpiconditionalformattingoption-syntax.json"></a>

```
{
  "[PrimaryValue](#cfn-quicksight-dashboard-kpiconditionalformattingoption-primaryvalue)" : KPIPrimaryValueConditionalFormatting,
  "[ProgressBar](#cfn-quicksight-dashboard-kpiconditionalformattingoption-progressbar)" : KPIProgressBarConditionalFormatting
}
```

### YAML<a name="aws-properties-quicksight-dashboard-kpiconditionalformattingoption-syntax.yaml"></a>

```
  [PrimaryValue](#cfn-quicksight-dashboard-kpiconditionalformattingoption-primaryvalue): 
    KPIPrimaryValueConditionalFormatting
  [ProgressBar](#cfn-quicksight-dashboard-kpiconditionalformattingoption-progressbar): 
    KPIProgressBarConditionalFormatting
```

## Properties<a name="aws-properties-quicksight-dashboard-kpiconditionalformattingoption-properties"></a>

`PrimaryValue`  <a name="cfn-quicksight-dashboard-kpiconditionalformattingoption-primaryvalue"></a>
The conditional formatting for the primary value of a KPI visual\.  
*Required*: No  
*Type*: [KPIPrimaryValueConditionalFormatting](aws-properties-quicksight-dashboard-kpiprimaryvalueconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProgressBar`  <a name="cfn-quicksight-dashboard-kpiconditionalformattingoption-progressbar"></a>
The conditional formatting for the progress bar of a KPI visual\.  
*Required*: No  
*Type*: [KPIProgressBarConditionalFormatting](aws-properties-quicksight-dashboard-kpiprogressbarconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)