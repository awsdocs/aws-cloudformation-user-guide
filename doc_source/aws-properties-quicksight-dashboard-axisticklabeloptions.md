# AWS::QuickSight::Dashboard AxisTickLabelOptions<a name="aws-properties-quicksight-dashboard-axisticklabeloptions"></a>

The tick label options of an axis\.

## Syntax<a name="aws-properties-quicksight-dashboard-axisticklabeloptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-axisticklabeloptions-syntax.json"></a>

```
{
  "[LabelOptions](#cfn-quicksight-dashboard-axisticklabeloptions-labeloptions)" : LabelOptions,
  "[RotationAngle](#cfn-quicksight-dashboard-axisticklabeloptions-rotationangle)" : Double
}
```

### YAML<a name="aws-properties-quicksight-dashboard-axisticklabeloptions-syntax.yaml"></a>

```
  [LabelOptions](#cfn-quicksight-dashboard-axisticklabeloptions-labeloptions): 
    LabelOptions
  [RotationAngle](#cfn-quicksight-dashboard-axisticklabeloptions-rotationangle): Double
```

## Properties<a name="aws-properties-quicksight-dashboard-axisticklabeloptions-properties"></a>

`LabelOptions`  <a name="cfn-quicksight-dashboard-axisticklabeloptions-labeloptions"></a>
Determines whether or not the axis ticks are visible\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-dashboard-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotationAngle`  <a name="cfn-quicksight-dashboard-axisticklabeloptions-rotationangle"></a>
The rotation angle of the axis tick labels\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)