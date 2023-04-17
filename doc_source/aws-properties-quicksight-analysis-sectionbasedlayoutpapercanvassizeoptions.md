# AWS::QuickSight::Analysis SectionBasedLayoutPaperCanvasSizeOptions<a name="aws-properties-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions"></a>

The options for a paper canvas of a section\-based layout\.

## Syntax<a name="aws-properties-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-syntax.json"></a>

```
{
  "[PaperMargin](#cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-papermargin)" : Spacing,
  "[PaperOrientation](#cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-paperorientation)" : String,
  "[PaperSize](#cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-papersize)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-syntax.yaml"></a>

```
  [PaperMargin](#cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-papermargin): 
    Spacing
  [PaperOrientation](#cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-paperorientation): String
  [PaperSize](#cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-papersize): String
```

## Properties<a name="aws-properties-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-properties"></a>

`PaperMargin`  <a name="cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-papermargin"></a>
Defines the spacing between the canvas content and the top, bottom, left, and right edges\.  
*Required*: No  
*Type*: [Spacing](aws-properties-quicksight-analysis-spacing.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaperOrientation`  <a name="cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-paperorientation"></a>
The paper orientation that is used to define canvas dimensions\. Choose one of the following options:  
+ PORTRAIT
+ LANDSCAPE
*Required*: No  
*Type*: String  
*Allowed values*: `LANDSCAPE | PORTRAIT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PaperSize`  <a name="cfn-quicksight-analysis-sectionbasedlayoutpapercanvassizeoptions-papersize"></a>
The paper size that is used to define canvas dimensions\.  
*Required*: No  
*Type*: String  
*Allowed values*: `A0 | A1 | A2 | A3 | A4 | A5 | JIS_B4 | JIS_B5 | US_LEGAL | US_LETTER | US_TABLOID_LEDGER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)