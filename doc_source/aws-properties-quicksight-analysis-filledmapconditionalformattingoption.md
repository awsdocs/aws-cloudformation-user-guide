# AWS::QuickSight::Analysis FilledMapConditionalFormattingOption<a name="aws-properties-quicksight-analysis-filledmapconditionalformattingoption"></a>

Conditional formatting options of a `FilledMapVisual`\.

## Syntax<a name="aws-properties-quicksight-analysis-filledmapconditionalformattingoption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-filledmapconditionalformattingoption-syntax.json"></a>

```
{
  "[Shape](#cfn-quicksight-analysis-filledmapconditionalformattingoption-shape)" : FilledMapShapeConditionalFormatting
}
```

### YAML<a name="aws-properties-quicksight-analysis-filledmapconditionalformattingoption-syntax.yaml"></a>

```
  [Shape](#cfn-quicksight-analysis-filledmapconditionalformattingoption-shape): 
    FilledMapShapeConditionalFormatting
```

## Properties<a name="aws-properties-quicksight-analysis-filledmapconditionalformattingoption-properties"></a>

`Shape`  <a name="cfn-quicksight-analysis-filledmapconditionalformattingoption-shape"></a>
The conditional formatting that determines the shape of the filled map\.  
*Required*: Yes  
*Type*: [FilledMapShapeConditionalFormatting](aws-properties-quicksight-analysis-filledmapshapeconditionalformatting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)