# AWS::QuickSight::Template ConditionalFormattingGradientColor<a name="aws-properties-quicksight-template-conditionalformattinggradientcolor"></a>

Formatting configuration for gradient color\.

## Syntax<a name="aws-properties-quicksight-template-conditionalformattinggradientcolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-conditionalformattinggradientcolor-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-template-conditionalformattinggradientcolor-color)" : GradientColor,
  "[Expression](#cfn-quicksight-template-conditionalformattinggradientcolor-expression)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-conditionalformattinggradientcolor-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-template-conditionalformattinggradientcolor-color): 
    GradientColor
  [Expression](#cfn-quicksight-template-conditionalformattinggradientcolor-expression): String
```

## Properties<a name="aws-properties-quicksight-template-conditionalformattinggradientcolor-properties"></a>

`Color`  <a name="cfn-quicksight-template-conditionalformattinggradientcolor-color"></a>
Determines the color\.  
*Required*: Yes  
*Type*: [GradientColor](aws-properties-quicksight-template-gradientcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-template-conditionalformattinggradientcolor-expression"></a>
The expression that determines the formatting configuration for gradient color\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)