# AWS::QuickSight::Template FilledMapConditionalFormatting<a name="aws-properties-quicksight-template-filledmapconditionalformatting"></a>

The conditional formatting of a `FilledMapVisual`\.

## Syntax<a name="aws-properties-quicksight-template-filledmapconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filledmapconditionalformatting-syntax.json"></a>

```
{
  "[ConditionalFormattingOptions](#cfn-quicksight-template-filledmapconditionalformatting-conditionalformattingoptions)" : [ FilledMapConditionalFormattingOption, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-filledmapconditionalformatting-syntax.yaml"></a>

```
  [ConditionalFormattingOptions](#cfn-quicksight-template-filledmapconditionalformatting-conditionalformattingoptions): 
    - FilledMapConditionalFormattingOption
```

## Properties<a name="aws-properties-quicksight-template-filledmapconditionalformatting-properties"></a>

`ConditionalFormattingOptions`  <a name="cfn-quicksight-template-filledmapconditionalformatting-conditionalformattingoptions"></a>
Conditional formatting options of a `FilledMapVisual`\.  
*Required*: Yes  
*Type*: List of [FilledMapConditionalFormattingOption](aws-properties-quicksight-template-filledmapconditionalformattingoption.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)