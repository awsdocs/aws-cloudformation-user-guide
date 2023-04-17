# AWS::QuickSight::Dashboard AxisScale<a name="aws-properties-quicksight-dashboard-axisscale"></a>

The scale setup options for a numeric axis display\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-axisscale-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-axisscale-syntax.json"></a>

```
{
  "[Linear](#cfn-quicksight-dashboard-axisscale-linear)" : AxisLinearScale,
  "[Logarithmic](#cfn-quicksight-dashboard-axisscale-logarithmic)" : AxisLogarithmicScale
}
```

### YAML<a name="aws-properties-quicksight-dashboard-axisscale-syntax.yaml"></a>

```
  [Linear](#cfn-quicksight-dashboard-axisscale-linear): 
    AxisLinearScale
  [Logarithmic](#cfn-quicksight-dashboard-axisscale-logarithmic): 
    AxisLogarithmicScale
```

## Properties<a name="aws-properties-quicksight-dashboard-axisscale-properties"></a>

`Linear`  <a name="cfn-quicksight-dashboard-axisscale-linear"></a>
The linear axis scale setup\.  
*Required*: No  
*Type*: [AxisLinearScale](aws-properties-quicksight-dashboard-axislinearscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logarithmic`  <a name="cfn-quicksight-dashboard-axisscale-logarithmic"></a>
The logarithmic axis scale setup\.  
*Required*: No  
*Type*: [AxisLogarithmicScale](aws-properties-quicksight-dashboard-axislogarithmicscale.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)