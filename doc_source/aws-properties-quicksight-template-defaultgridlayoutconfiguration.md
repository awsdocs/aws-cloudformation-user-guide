# AWS::QuickSight::Template DefaultGridLayoutConfiguration<a name="aws-properties-quicksight-template-defaultgridlayoutconfiguration"></a>

The options that determine the default settings for a grid layout configuration\.

## Syntax<a name="aws-properties-quicksight-template-defaultgridlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-defaultgridlayoutconfiguration-syntax.json"></a>

```
{
  "[CanvasSizeOptions](#cfn-quicksight-template-defaultgridlayoutconfiguration-canvassizeoptions)" : GridLayoutCanvasSizeOptions
}
```

### YAML<a name="aws-properties-quicksight-template-defaultgridlayoutconfiguration-syntax.yaml"></a>

```
  [CanvasSizeOptions](#cfn-quicksight-template-defaultgridlayoutconfiguration-canvassizeoptions): 
    GridLayoutCanvasSizeOptions
```

## Properties<a name="aws-properties-quicksight-template-defaultgridlayoutconfiguration-properties"></a>

`CanvasSizeOptions`  <a name="cfn-quicksight-template-defaultgridlayoutconfiguration-canvassizeoptions"></a>
Determines the screen canvas size options for a grid layout\.  
*Required*: Yes  
*Type*: [GridLayoutCanvasSizeOptions](aws-properties-quicksight-template-gridlayoutcanvassizeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)