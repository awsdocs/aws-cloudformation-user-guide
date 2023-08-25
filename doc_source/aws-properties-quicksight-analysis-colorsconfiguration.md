# AWS::QuickSight::Analysis ColorsConfiguration<a name="aws-properties-quicksight-analysis-colorsconfiguration"></a>

The color configurations for a column\.

## Syntax<a name="aws-properties-quicksight-analysis-colorsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-colorsconfiguration-syntax.json"></a>

```
{
  "[CustomColors](#cfn-quicksight-analysis-colorsconfiguration-customcolors)" : [ CustomColor, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-colorsconfiguration-syntax.yaml"></a>

```
  [CustomColors](#cfn-quicksight-analysis-colorsconfiguration-customcolors): 
    - CustomColor
```

## Properties<a name="aws-properties-quicksight-analysis-colorsconfiguration-properties"></a>

`CustomColors`  <a name="cfn-quicksight-analysis-colorsconfiguration-customcolors"></a>
A list of up to 50 custom colors\.  
*Required*: No  
*Type*: List of [CustomColor](aws-properties-quicksight-analysis-customcolor.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)