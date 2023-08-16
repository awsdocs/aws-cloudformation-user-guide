# AWS::QuickSight::Template AxisScale<a name="aws-properties-quicksight-template-axisscale"></a>

The scale setup options for a numeric axis display\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-axisscale-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-axisscale-syntax.json"></a>

```
{
  "[Linear](#cfn-quicksight-template-axisscale-linear)" : AxisLinearScale,
  "[Logarithmic](#cfn-quicksight-template-axisscale-logarithmic)" : AxisLogarithmicScale
}
```

### YAML<a name="aws-properties-quicksight-template-axisscale-syntax.yaml"></a>

```
  [Linear](#cfn-quicksight-template-axisscale-linear): 
    AxisLinearScale
  [Logarithmic](#cfn-quicksight-template-axisscale-logarithmic): 
    AxisLogarithmicScale
```

## Properties<a name="aws-properties-quicksight-template-axisscale-properties"></a>

`Linear`  <a name="cfn-quicksight-template-axisscale-linear"></a>
The linear axis scale setup\.  
*Required*: No  
*Type*: [AxisLinearScale](aws-properties-quicksight-template-axislinearscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logarithmic`  <a name="cfn-quicksight-template-axisscale-logarithmic"></a>
The logarithmic axis scale setup\.  
*Required*: No  
*Type*: [AxisLogarithmicScale](aws-properties-quicksight-template-axislogarithmicscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)