# AWS::QuickSight::Template PercentVisibleRange<a name="aws-properties-quicksight-template-percentvisiblerange"></a>

The percent range in the visible range\.

## Syntax<a name="aws-properties-quicksight-template-percentvisiblerange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-percentvisiblerange-syntax.json"></a>

```
{
  "[From](#cfn-quicksight-template-percentvisiblerange-from)" : Double,
  "[To](#cfn-quicksight-template-percentvisiblerange-to)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-percentvisiblerange-syntax.yaml"></a>

```
  [From](#cfn-quicksight-template-percentvisiblerange-from): Double
  [To](#cfn-quicksight-template-percentvisiblerange-to): Double
```

## Properties<a name="aws-properties-quicksight-template-percentvisiblerange-properties"></a>

`From`  <a name="cfn-quicksight-template-percentvisiblerange-from"></a>
The lower bound of the range\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`To`  <a name="cfn-quicksight-template-percentvisiblerange-to"></a>
The top bound of the range\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)