# AWS::QuickSight::Dashboard GradientStop<a name="aws-properties-quicksight-dashboard-gradientstop"></a>

Determines the gradient stop configuration\.

## Syntax<a name="aws-properties-quicksight-dashboard-gradientstop-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-gradientstop-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-dashboard-gradientstop-color)" : String,
  "[DataValue](#cfn-quicksight-dashboard-gradientstop-datavalue)" : Double,
  "[GradientOffset](#cfn-quicksight-dashboard-gradientstop-gradientoffset)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-gradientstop-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-dashboard-gradientstop-color): String
  [DataValue](#cfn-quicksight-dashboard-gradientstop-datavalue): Double
  [GradientOffset](#cfn-quicksight-dashboard-gradientstop-gradientoffset): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-gradientstop-properties"></a>

`Color`  <a name="cfn-quicksight-dashboard-gradientstop-color"></a>
Determines the color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataValue`  <a name="cfn-quicksight-dashboard-gradientstop-datavalue"></a>
Determines the data value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GradientOffset`  <a name="cfn-quicksight-dashboard-gradientstop-gradientoffset"></a>
Determines gradient offset value\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)