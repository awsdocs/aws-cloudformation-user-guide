# AWS::QuickSight::Theme SheetStyle<a name="aws-properties-quicksight-theme-sheetstyle"></a>

The theme display options for sheets\. 

## Syntax<a name="aws-properties-quicksight-theme-sheetstyle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-theme-sheetstyle-syntax.json"></a>

```
{
  "[Tile](#cfn-quicksight-theme-sheetstyle-tile)" : TileStyle,
  "[TileLayout](#cfn-quicksight-theme-sheetstyle-tilelayout)" : TileLayoutStyle
}
```

### YAML<a name="aws-properties-quicksight-theme-sheetstyle-syntax.yaml"></a>

```
  [Tile](#cfn-quicksight-theme-sheetstyle-tile): 
    TileStyle
  [TileLayout](#cfn-quicksight-theme-sheetstyle-tilelayout): 
    TileLayoutStyle
```

## Properties<a name="aws-properties-quicksight-theme-sheetstyle-properties"></a>

`Tile`  <a name="cfn-quicksight-theme-sheetstyle-tile"></a>
The display options for tiles\.  
*Required*: No  
*Type*: [TileStyle](aws-properties-quicksight-theme-tilestyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TileLayout`  <a name="cfn-quicksight-theme-sheetstyle-tilelayout"></a>
The layout options for tiles\.  
*Required*: No  
*Type*: [TileLayoutStyle](aws-properties-quicksight-theme-tilelayoutstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)