# AWS::QuickSight::Analysis ConditionalFormattingIconSet<a name="aws-properties-quicksight-analysis-conditionalformattingiconset"></a>

Formatting configuration for icon set\.

## Syntax<a name="aws-properties-quicksight-analysis-conditionalformattingiconset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-conditionalformattingiconset-syntax.json"></a>

```
{
  "[Expression](#cfn-quicksight-analysis-conditionalformattingiconset-expression)" : String,
  "[IconSetType](#cfn-quicksight-analysis-conditionalformattingiconset-iconsettype)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-conditionalformattingiconset-syntax.yaml"></a>

```
  [Expression](#cfn-quicksight-analysis-conditionalformattingiconset-expression): String
  [IconSetType](#cfn-quicksight-analysis-conditionalformattingiconset-iconsettype): String
```

## Properties<a name="aws-properties-quicksight-analysis-conditionalformattingiconset-properties"></a>

`Expression`  <a name="cfn-quicksight-analysis-conditionalformattingiconset-expression"></a>
The expression that determines the formatting configuration for the icon set\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IconSetType`  <a name="cfn-quicksight-analysis-conditionalformattingiconset-iconsettype"></a>
Determines the icon set type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `BARS | CARET_UP_MINUS_DOWN | CHECK_X | FLAGS | FOUR_COLOR_ARROW | FOUR_GRAY_ARROW | PLUS_MINUS | THREE_CIRCLE | THREE_COLOR_ARROW | THREE_GRAY_ARROW | THREE_SHAPE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)