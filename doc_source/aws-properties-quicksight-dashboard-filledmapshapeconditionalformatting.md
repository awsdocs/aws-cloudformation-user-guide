# AWS::QuickSight::Dashboard FilledMapShapeConditionalFormatting<a name="aws-properties-quicksight-dashboard-filledmapshapeconditionalformatting"></a>

The conditional formatting that determines the shape of the filled map\.

## Syntax<a name="aws-properties-quicksight-dashboard-filledmapshapeconditionalformatting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filledmapshapeconditionalformatting-syntax.json"></a>

```
{
  "[FieldId](#cfn-quicksight-dashboard-filledmapshapeconditionalformatting-fieldid)" : String,
  "[Format](#cfn-quicksight-dashboard-filledmapshapeconditionalformatting-format)" : ShapeConditionalFormat
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filledmapshapeconditionalformatting-syntax.yaml"></a>

```
  [FieldId](#cfn-quicksight-dashboard-filledmapshapeconditionalformatting-fieldid): String
  [Format](#cfn-quicksight-dashboard-filledmapshapeconditionalformatting-format): 
    ShapeConditionalFormat
```

## Properties<a name="aws-properties-quicksight-dashboard-filledmapshapeconditionalformatting-properties"></a>

`FieldId`  <a name="cfn-quicksight-dashboard-filledmapshapeconditionalformatting-fieldid"></a>
The field ID of the filled map shape\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-quicksight-dashboard-filledmapshapeconditionalformatting-format"></a>
The conditional formatting that determines the background color of a filled map's shape\.  
*Required*: No  
*Type*: [ShapeConditionalFormat](aws-properties-quicksight-dashboard-shapeconditionalformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)