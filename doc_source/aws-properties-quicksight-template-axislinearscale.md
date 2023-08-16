# AWS::QuickSight::Template AxisLinearScale<a name="aws-properties-quicksight-template-axislinearscale"></a>

The liner axis scale setup\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-axislinearscale-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-axislinearscale-syntax.json"></a>

```
{
  "[StepCount](#cfn-quicksight-template-axislinearscale-stepcount)" : Double,
  "[StepSize](#cfn-quicksight-template-axislinearscale-stepsize)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-axislinearscale-syntax.yaml"></a>

```
  [StepCount](#cfn-quicksight-template-axislinearscale-stepcount): Double
  [StepSize](#cfn-quicksight-template-axislinearscale-stepsize): Double
```

## Properties<a name="aws-properties-quicksight-template-axislinearscale-properties"></a>

`StepCount`  <a name="cfn-quicksight-template-axislinearscale-stepcount"></a>
The step count setup of a linear axis\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepSize`  <a name="cfn-quicksight-template-axislinearscale-stepsize"></a>
The step size setup of a linear axis\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)