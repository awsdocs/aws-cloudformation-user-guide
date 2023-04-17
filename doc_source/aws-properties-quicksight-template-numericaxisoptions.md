# AWS::QuickSight::Template NumericAxisOptions<a name="aws-properties-quicksight-template-numericaxisoptions"></a>

The options for an axis with a numeric field\.

## Syntax<a name="aws-properties-quicksight-template-numericaxisoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-numericaxisoptions-syntax.json"></a>

```
{
  "[Range](#cfn-quicksight-template-numericaxisoptions-range)" : AxisDisplayRange,
  "[Scale](#cfn-quicksight-template-numericaxisoptions-scale)" : AxisScale
}
```

### YAML<a name="aws-properties-quicksight-template-numericaxisoptions-syntax.yaml"></a>

```
  [Range](#cfn-quicksight-template-numericaxisoptions-range): 
    AxisDisplayRange
  [Scale](#cfn-quicksight-template-numericaxisoptions-scale): 
    AxisScale
```

## Properties<a name="aws-properties-quicksight-template-numericaxisoptions-properties"></a>

`Range`  <a name="cfn-quicksight-template-numericaxisoptions-range"></a>
The range setup of a numeric axis\.  
*Required*: No  
*Type*: [AxisDisplayRange](aws-properties-quicksight-template-axisdisplayrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scale`  <a name="cfn-quicksight-template-numericaxisoptions-scale"></a>
The scale setup of a numeric axis\.  
*Required*: No  
*Type*: [AxisScale](aws-properties-quicksight-template-axisscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)