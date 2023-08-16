# AWS::QuickSight::Analysis ShapeConditionalFormat<a name="aws-properties-quicksight-analysis-shapeconditionalformat"></a>

The shape conditional formatting of a filled map visual\.

## Syntax<a name="aws-properties-quicksight-analysis-shapeconditionalformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-shapeconditionalformat-syntax.json"></a>

```
{
  "[BackgroundColor](#cfn-quicksight-analysis-shapeconditionalformat-backgroundcolor)" : ConditionalFormattingColor
}
```

### YAML<a name="aws-properties-quicksight-analysis-shapeconditionalformat-syntax.yaml"></a>

```
  [BackgroundColor](#cfn-quicksight-analysis-shapeconditionalformat-backgroundcolor): 
    ConditionalFormattingColor
```

## Properties<a name="aws-properties-quicksight-analysis-shapeconditionalformat-properties"></a>

`BackgroundColor`  <a name="cfn-quicksight-analysis-shapeconditionalformat-backgroundcolor"></a>
The conditional formatting for the shape background color of a filled map visual\.  
*Required*: Yes  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-analysis-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)