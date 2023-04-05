# AWS::QuickSight::Template KPIProgressBarConditionalFormatting<a name="aws-properties-quicksight-template-kpiprogressbarconditionalformatting"></a>

The conditional formatting for the progress bar of a KPI visual\.

## Syntax<a name="aws-properties-quicksight-template-kpiprogressbarconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-kpiprogressbarconditionalformatting-syntax.json"></a>

```
{
  "[ForegroundColor](#cfn-quicksight-template-kpiprogressbarconditionalformatting-foregroundcolor)" : ConditionalFormattingColor
}
```

### YAML<a name="aws-properties-quicksight-template-kpiprogressbarconditionalformatting-syntax.yaml"></a>

```
  [ForegroundColor](#cfn-quicksight-template-kpiprogressbarconditionalformatting-foregroundcolor): 
    ConditionalFormattingColor
```

## Properties<a name="aws-properties-quicksight-template-kpiprogressbarconditionalformatting-properties"></a>

`ForegroundColor`  <a name="cfn-quicksight-template-kpiprogressbarconditionalformatting-foregroundcolor"></a>
The conditional formatting of the progress bar's foreground color\.  
*Required*: No  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-template-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)