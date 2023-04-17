# AWS::QuickSight::Template FreeFormLayoutConfiguration<a name="aws-properties-quicksight-template-freeformlayoutconfiguration"></a>

The configuration of a free\-form layout\.

## Syntax<a name="aws-properties-quicksight-template-freeformlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-freeformlayoutconfiguration-syntax.json"></a>

```
{
  "[CanvasSizeOptions](#cfn-quicksight-template-freeformlayoutconfiguration-canvassizeoptions)" : FreeFormLayoutCanvasSizeOptions,
  "[Elements](#cfn-quicksight-template-freeformlayoutconfiguration-elements)" : [ FreeFormLayoutElement, ... ]
}
```

### YAML<a name="aws-properties-quicksight-template-freeformlayoutconfiguration-syntax.yaml"></a>

```
  [CanvasSizeOptions](#cfn-quicksight-template-freeformlayoutconfiguration-canvassizeoptions): 
    FreeFormLayoutCanvasSizeOptions
  [Elements](#cfn-quicksight-template-freeformlayoutconfiguration-elements): 
    - FreeFormLayoutElement
```

## Properties<a name="aws-properties-quicksight-template-freeformlayoutconfiguration-properties"></a>

`CanvasSizeOptions`  <a name="cfn-quicksight-template-freeformlayoutconfiguration-canvassizeoptions"></a>
Property description not available\.  
*Required*: No  
*Type*: [FreeFormLayoutCanvasSizeOptions](aws-properties-quicksight-template-freeformlayoutcanvassizeoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Elements`  <a name="cfn-quicksight-template-freeformlayoutconfiguration-elements"></a>
The elements that are included in a free\-form layout\.  
*Required*: Yes  
*Type*: List of [FreeFormLayoutElement](aws-properties-quicksight-template-freeformlayoutelement.md)  
*Maximum*: `430`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)