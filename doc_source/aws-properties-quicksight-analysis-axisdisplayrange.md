# AWS::QuickSight::Analysis AxisDisplayRange<a name="aws-properties-quicksight-analysis-axisdisplayrange"></a>

The range setup of a numeric axis display range\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-axisdisplayrange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-axisdisplayrange-syntax.json"></a>

```
{
  "[DataDriven](#cfn-quicksight-analysis-axisdisplayrange-datadriven)" : Json,
  "[MinMax](#cfn-quicksight-analysis-axisdisplayrange-minmax)" : AxisDisplayMinMaxRange
}
```

### YAML<a name="aws-properties-quicksight-analysis-axisdisplayrange-syntax.yaml"></a>

```
  [DataDriven](#cfn-quicksight-analysis-axisdisplayrange-datadriven): Json
  [MinMax](#cfn-quicksight-analysis-axisdisplayrange-minmax): 
    AxisDisplayMinMaxRange
```

## Properties<a name="aws-properties-quicksight-analysis-axisdisplayrange-properties"></a>

`DataDriven`  <a name="cfn-quicksight-analysis-axisdisplayrange-datadriven"></a>
The data\-driven setup of an axis display range\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinMax`  <a name="cfn-quicksight-analysis-axisdisplayrange-minmax"></a>
The minimum and maximum setup of an axis display range\.  
*Required*: No  
*Type*: [AxisDisplayMinMaxRange](aws-properties-quicksight-analysis-axisdisplayminmaxrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)