# AWS::QuickSight::Dashboard ShapeConditionalFormat<a name="aws-properties-quicksight-dashboard-shapeconditionalformat"></a>

The shape conditional formatting of a filled map visual\.

## Syntax<a name="aws-properties-quicksight-dashboard-shapeconditionalformat-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-shapeconditionalformat-syntax.json"></a>

```
{
  "[BackgroundColor](#cfn-quicksight-dashboard-shapeconditionalformat-backgroundcolor)" : ConditionalFormattingColor
}
```

### YAML<a name="aws-properties-quicksight-dashboard-shapeconditionalformat-syntax.yaml"></a>

```
  [BackgroundColor](#cfn-quicksight-dashboard-shapeconditionalformat-backgroundcolor): 
    ConditionalFormattingColor
```

## Properties<a name="aws-properties-quicksight-dashboard-shapeconditionalformat-properties"></a>

`BackgroundColor`  <a name="cfn-quicksight-dashboard-shapeconditionalformat-backgroundcolor"></a>
The conditional formatting for the shape background color of a filled map visual\.  
*Required*: Yes  
*Type*: [ConditionalFormattingColor](aws-properties-quicksight-dashboard-conditionalformattingcolor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)