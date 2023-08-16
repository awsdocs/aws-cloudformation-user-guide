# AWS::QuickSight::Template DefaultFreeFormLayoutConfiguration<a name="aws-properties-quicksight-template-defaultfreeformlayoutconfiguration"></a>

The options that determine the default settings of a free\-form layout configuration\.

## Syntax<a name="aws-properties-quicksight-template-defaultfreeformlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-defaultfreeformlayoutconfiguration-syntax.json"></a>

```
{
  "[CanvasSizeOptions](#cfn-quicksight-template-defaultfreeformlayoutconfiguration-canvassizeoptions)" : FreeFormLayoutCanvasSizeOptions
}
```

### YAML<a name="aws-properties-quicksight-template-defaultfreeformlayoutconfiguration-syntax.yaml"></a>

```
  [CanvasSizeOptions](#cfn-quicksight-template-defaultfreeformlayoutconfiguration-canvassizeoptions): 
    FreeFormLayoutCanvasSizeOptions
```

## Properties<a name="aws-properties-quicksight-template-defaultfreeformlayoutconfiguration-properties"></a>

`CanvasSizeOptions`  <a name="cfn-quicksight-template-defaultfreeformlayoutconfiguration-canvassizeoptions"></a>
Determines the screen canvas size options for a free\-form layout\.  
*Required*: Yes  
*Type*: [FreeFormLayoutCanvasSizeOptions](aws-properties-quicksight-template-freeformlayoutcanvassizeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)