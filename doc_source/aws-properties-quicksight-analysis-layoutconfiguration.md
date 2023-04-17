# AWS::QuickSight::Analysis LayoutConfiguration<a name="aws-properties-quicksight-analysis-layoutconfiguration"></a>

The configuration that determines what the type of layout will be used on a sheet\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-analysis-layoutconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-layoutconfiguration-syntax.json"></a>

```
{
  "[FreeFormLayout](#cfn-quicksight-analysis-layoutconfiguration-freeformlayout)" : FreeFormLayoutConfiguration,
  "[GridLayout](#cfn-quicksight-analysis-layoutconfiguration-gridlayout)" : GridLayoutConfiguration,
  "[SectionBasedLayout](#cfn-quicksight-analysis-layoutconfiguration-sectionbasedlayout)" : SectionBasedLayoutConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-layoutconfiguration-syntax.yaml"></a>

```
  [FreeFormLayout](#cfn-quicksight-analysis-layoutconfiguration-freeformlayout): 
    FreeFormLayoutConfiguration
  [GridLayout](#cfn-quicksight-analysis-layoutconfiguration-gridlayout): 
    GridLayoutConfiguration
  [SectionBasedLayout](#cfn-quicksight-analysis-layoutconfiguration-sectionbasedlayout): 
    SectionBasedLayoutConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-layoutconfiguration-properties"></a>

`FreeFormLayout`  <a name="cfn-quicksight-analysis-layoutconfiguration-freeformlayout"></a>
A free\-form is optimized for a fixed width and has more control over the exact placement of layout elements\.  
*Required*: No  
*Type*: [FreeFormLayoutConfiguration](aws-properties-quicksight-analysis-freeformlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GridLayout`  <a name="cfn-quicksight-analysis-layoutconfiguration-gridlayout"></a>
A type of layout that can be used on a sheet\. In a grid layout, visuals snap to a grid with standard spacing and alignment\. Dashboards are displayed as designed, with options to fit to screen or view at actual size\. A grid layout can be configured to behave in one of two ways when the viewport is resized: `FIXED` or `RESPONSIVE`\.  
*Required*: No  
*Type*: [GridLayoutConfiguration](aws-properties-quicksight-analysis-gridlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SectionBasedLayout`  <a name="cfn-quicksight-analysis-layoutconfiguration-sectionbasedlayout"></a>
A section based layout organizes visuals into multiple sections and has customized header, footer and page break\.  
*Required*: No  
*Type*: [SectionBasedLayoutConfiguration](aws-properties-quicksight-analysis-sectionbasedlayoutconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)