# AWS::QuickSight::Dashboard ConditionalFormattingSolidColor<a name="aws-properties-quicksight-dashboard-conditionalformattingsolidcolor"></a>

Formatting configuration for solid color\.

## Syntax<a name="aws-properties-quicksight-dashboard-conditionalformattingsolidcolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-conditionalformattingsolidcolor-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-dashboard-conditionalformattingsolidcolor-color)" : String,
  "[Expression](#cfn-quicksight-dashboard-conditionalformattingsolidcolor-expression)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-conditionalformattingsolidcolor-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-dashboard-conditionalformattingsolidcolor-color): String
  [Expression](#cfn-quicksight-dashboard-conditionalformattingsolidcolor-expression): String
```

## Properties<a name="aws-properties-quicksight-dashboard-conditionalformattingsolidcolor-properties"></a>

`Color`  <a name="cfn-quicksight-dashboard-conditionalformattingsolidcolor-color"></a>
Determines the color\.  
*Required*: No  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-dashboard-conditionalformattingsolidcolor-expression"></a>
The expression that determines the formatting configuration for solid color\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)