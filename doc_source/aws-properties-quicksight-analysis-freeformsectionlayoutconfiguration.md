# AWS::QuickSight::Analysis FreeFormSectionLayoutConfiguration<a name="aws-properties-quicksight-analysis-freeformsectionlayoutconfiguration"></a>

The free\-form layout configuration of a section\.

## Syntax<a name="aws-properties-quicksight-analysis-freeformsectionlayoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-freeformsectionlayoutconfiguration-syntax.json"></a>

```
{
  "[Elements](#cfn-quicksight-analysis-freeformsectionlayoutconfiguration-elements)" : [ FreeFormLayoutElement, ... ]
}
```

### YAML<a name="aws-properties-quicksight-analysis-freeformsectionlayoutconfiguration-syntax.yaml"></a>

```
  [Elements](#cfn-quicksight-analysis-freeformsectionlayoutconfiguration-elements): 
    - FreeFormLayoutElement
```

## Properties<a name="aws-properties-quicksight-analysis-freeformsectionlayoutconfiguration-properties"></a>

`Elements`  <a name="cfn-quicksight-analysis-freeformsectionlayoutconfiguration-elements"></a>
The elements that are included in the free\-form layout\.  
*Required*: Yes  
*Type*: List of [FreeFormLayoutElement](aws-properties-quicksight-analysis-freeformlayoutelement.md)  
*Maximum*: `430`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)