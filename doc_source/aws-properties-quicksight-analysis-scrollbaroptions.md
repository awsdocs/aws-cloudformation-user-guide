# AWS::QuickSight::Analysis ScrollBarOptions<a name="aws-properties-quicksight-analysis-scrollbaroptions"></a>

The visual display options for a data zoom scroll bar\.

## Syntax<a name="aws-properties-quicksight-analysis-scrollbaroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-scrollbaroptions-syntax.json"></a>

```
{
  "[Visibility](#cfn-quicksight-analysis-scrollbaroptions-visibility)" : String,
  "[VisibleRange](#cfn-quicksight-analysis-scrollbaroptions-visiblerange)" : VisibleRangeOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-scrollbaroptions-syntax.yaml"></a>

```
  [Visibility](#cfn-quicksight-analysis-scrollbaroptions-visibility): String
  [VisibleRange](#cfn-quicksight-analysis-scrollbaroptions-visiblerange): 
    VisibleRangeOptions
```

## Properties<a name="aws-properties-quicksight-analysis-scrollbaroptions-properties"></a>

`Visibility`  <a name="cfn-quicksight-analysis-scrollbaroptions-visibility"></a>
The visibility of the data zoom scroll bar\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisibleRange`  <a name="cfn-quicksight-analysis-scrollbaroptions-visiblerange"></a>
The visibility range for the data zoom scroll bar\.  
*Required*: No  
*Type*: [VisibleRangeOptions](aws-properties-quicksight-analysis-visiblerangeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)