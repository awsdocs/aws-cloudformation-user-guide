# AWS::QuickSight::Analysis SheetControlInfoIconLabelOptions<a name="aws-properties-quicksight-analysis-sheetcontrolinfoiconlabeloptions"></a>

A control to display info icons for filters and parameters\.

## Syntax<a name="aws-properties-quicksight-analysis-sheetcontrolinfoiconlabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sheetcontrolinfoiconlabeloptions-syntax.json"></a>

```
{
  "[InfoIconText](#cfn-quicksight-analysis-sheetcontrolinfoiconlabeloptions-infoicontext)" : String,
  "[Visibility](#cfn-quicksight-analysis-sheetcontrolinfoiconlabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-sheetcontrolinfoiconlabeloptions-syntax.yaml"></a>

```
  [InfoIconText](#cfn-quicksight-analysis-sheetcontrolinfoiconlabeloptions-infoicontext): String
  [Visibility](#cfn-quicksight-analysis-sheetcontrolinfoiconlabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-analysis-sheetcontrolinfoiconlabeloptions-properties"></a>

`InfoIconText`  <a name="cfn-quicksight-analysis-sheetcontrolinfoiconlabeloptions-infoicontext"></a>
 The text content of info icon\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-analysis-sheetcontrolinfoiconlabeloptions-visibility"></a>
The visibility configuration of info icon label options\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)