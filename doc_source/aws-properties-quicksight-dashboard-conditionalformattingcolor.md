# AWS::QuickSight::Dashboard ConditionalFormattingColor<a name="aws-properties-quicksight-dashboard-conditionalformattingcolor"></a>

The formatting configuration for the color\.

## Syntax<a name="aws-properties-quicksight-dashboard-conditionalformattingcolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-conditionalformattingcolor-syntax.json"></a>

```
{
  "[Gradient](#cfn-quicksight-dashboard-conditionalformattingcolor-gradient)" : ConditionalFormattingGradientColor,
  "[Solid](#cfn-quicksight-dashboard-conditionalformattingcolor-solid)" : ConditionalFormattingSolidColor
}
```

### YAML<a name="aws-properties-quicksight-dashboard-conditionalformattingcolor-syntax.yaml"></a>

```
  [Gradient](#cfn-quicksight-dashboard-conditionalformattingcolor-gradient): 
    ConditionalFormattingGradientColor
  [Solid](#cfn-quicksight-dashboard-conditionalformattingcolor-solid): 
    ConditionalFormattingSolidColor
```

## Properties<a name="aws-properties-quicksight-dashboard-conditionalformattingcolor-properties"></a>

`Gradient`  <a name="cfn-quicksight-dashboard-conditionalformattingcolor-gradient"></a>
Formatting configuration for gradient color\.  
*Required*: No  
*Type*: [ConditionalFormattingGradientColor](aws-properties-quicksight-dashboard-conditionalformattinggradientcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Solid`  <a name="cfn-quicksight-dashboard-conditionalformattingcolor-solid"></a>
Formatting configuration for solid color\.  
*Required*: No  
*Type*: [ConditionalFormattingSolidColor](aws-properties-quicksight-dashboard-conditionalformattingsolidcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)