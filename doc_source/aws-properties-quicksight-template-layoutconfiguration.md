# AWS::QuickSight::Template LayoutConfiguration<a name="aws-properties-quicksight-template-layoutconfiguration"></a>

The configuration that determines what the type of layout will be used on a sheet\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-template-layoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-layoutconfiguration-syntax.json"></a>

```
{
  "[FreeFormLayout](#cfn-quicksight-template-layoutconfiguration-freeformlayout)" : FreeFormLayoutConfiguration,
  "[GridLayout](#cfn-quicksight-template-layoutconfiguration-gridlayout)" : GridLayoutConfiguration,
  "[SectionBasedLayout](#cfn-quicksight-template-layoutconfiguration-sectionbasedlayout)" : SectionBasedLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-layoutconfiguration-syntax.yaml"></a>

```
  [FreeFormLayout](#cfn-quicksight-template-layoutconfiguration-freeformlayout): 
    FreeFormLayoutConfiguration
  [GridLayout](#cfn-quicksight-template-layoutconfiguration-gridlayout): 
    GridLayoutConfiguration
  [SectionBasedLayout](#cfn-quicksight-template-layoutconfiguration-sectionbasedlayout): 
    SectionBasedLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-template-layoutconfiguration-properties"></a>

`FreeFormLayout`  <a name="cfn-quicksight-template-layoutconfiguration-freeformlayout"></a>
A free\-form is optimized for a fixed width and has more control over the exact placement of layout elements\.  
*Required*: No  
*Type*: [FreeFormLayoutConfiguration](aws-properties-quicksight-template-freeformlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GridLayout`  <a name="cfn-quicksight-template-layoutconfiguration-gridlayout"></a>
A type of layout that can be used on a sheet\. In a grid layout, visuals snap to a grid with standard spacing and alignment\. Dashboards are displayed as designed, with options to fit to screen or view at actual size\. A grid layout can be configured to behave in one of two ways when the viewport is resized: `FIXED` or `RESPONSIVE`\.  
*Required*: No  
*Type*: [GridLayoutConfiguration](aws-properties-quicksight-template-gridlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SectionBasedLayout`  <a name="cfn-quicksight-template-layoutconfiguration-sectionbasedlayout"></a>
A section based layout organizes visuals into multiple sections and has customized header, footer and page break\.  
*Required*: No  
*Type*: [SectionBasedLayoutConfiguration](aws-properties-quicksight-template-sectionbasedlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)