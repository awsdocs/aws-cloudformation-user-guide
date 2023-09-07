# AWS::QuickSight::Analysis PivotTableRowsLabelOptions<a name="aws-properties-quicksight-analysis-pivottablerowslabeloptions"></a>

The options for the label thta is located above the row headers\. This option is only applicable when `RowsLayout` is set to `HIERARCHY`\.

## Syntax<a name="aws-properties-quicksight-analysis-pivottablerowslabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-pivottablerowslabeloptions-syntax.json"></a>

```
{
  "[CustomLabel](#cfn-quicksight-analysis-pivottablerowslabeloptions-customlabel)" : String,
  "[Visibility](#cfn-quicksight-analysis-pivottablerowslabeloptions-visibility)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-pivottablerowslabeloptions-syntax.yaml"></a>

```
  [CustomLabel](#cfn-quicksight-analysis-pivottablerowslabeloptions-customlabel): String
  [Visibility](#cfn-quicksight-analysis-pivottablerowslabeloptions-visibility): String
```

## Properties<a name="aws-properties-quicksight-analysis-pivottablerowslabeloptions-properties"></a>

`CustomLabel`  <a name="cfn-quicksight-analysis-pivottablerowslabeloptions-customlabel"></a>
The custom label string for the rows label\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-analysis-pivottablerowslabeloptions-visibility"></a>
The visibility of the rows label\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)