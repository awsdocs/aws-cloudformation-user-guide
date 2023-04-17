# AWS::QuickSight::Analysis AxisLinearScale<a name="aws-properties-quicksight-analysis-axislinearscale"></a>

The liner axis scale setup\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-axislinearscale-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-axislinearscale-syntax.json"></a>

```
{
  "[StepCount](#cfn-quicksight-analysis-axislinearscale-stepcount)" : Double,
  "[StepSize](#cfn-quicksight-analysis-axislinearscale-stepsize)" : Double
}
```

### YAML<a name="aws-properties-quicksight-analysis-axislinearscale-syntax.yaml"></a>

```
  [StepCount](#cfn-quicksight-analysis-axislinearscale-stepcount): Double
  [StepSize](#cfn-quicksight-analysis-axislinearscale-stepsize): Double
```

## Properties<a name="aws-properties-quicksight-analysis-axislinearscale-properties"></a>

`StepCount`  <a name="cfn-quicksight-analysis-axislinearscale-stepcount"></a>
The step count setup of a linear axis\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepSize`  <a name="cfn-quicksight-analysis-axislinearscale-stepsize"></a>
The step size setup of a linear axis\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)