# AWS::QuickSight::Dashboard GradientColor<a name="aws-properties-quicksight-dashboard-gradientcolor"></a>

Determines the gradient color settings\.

## Syntax<a name="aws-properties-quicksight-dashboard-gradientcolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-gradientcolor-syntax.json"></a>

```
{
  "[Stops](#cfn-quicksight-dashboard-gradientcolor-stops)" : [ GradientStop, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-gradientcolor-syntax.yaml"></a>

```
  [Stops](#cfn-quicksight-dashboard-gradientcolor-stops): 
    - GradientStop
```

## Properties<a name="aws-properties-quicksight-dashboard-gradientcolor-properties"></a>

`Stops`  <a name="cfn-quicksight-dashboard-gradientcolor-stops"></a>
The list of gradient color stops\.  
*Required*: No  
*Type*: List of [GradientStop](aws-properties-quicksight-dashboard-gradientstop.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)