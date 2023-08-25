# AWS::QuickSight::Dashboard ColorsConfiguration<a name="aws-properties-quicksight-dashboard-colorsconfiguration"></a>

The color configurations for a column\.

## Syntax<a name="aws-properties-quicksight-dashboard-colorsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-colorsconfiguration-syntax.json"></a>

```
{
  "[CustomColors](#cfn-quicksight-dashboard-colorsconfiguration-customcolors)" : [ CustomColor, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-colorsconfiguration-syntax.yaml"></a>

```
  [CustomColors](#cfn-quicksight-dashboard-colorsconfiguration-customcolors): 
    - CustomColor
```

## Properties<a name="aws-properties-quicksight-dashboard-colorsconfiguration-properties"></a>

`CustomColors`  <a name="cfn-quicksight-dashboard-colorsconfiguration-customcolors"></a>
A list of up to 50 custom colors\.  
*Required*: No  
*Type*: List of [CustomColor](aws-properties-quicksight-dashboard-customcolor.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)