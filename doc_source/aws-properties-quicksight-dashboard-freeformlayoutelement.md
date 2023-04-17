# AWS::QuickSight::Dashboard FreeFormLayoutElement<a name="aws-properties-quicksight-dashboard-freeformlayoutelement"></a>

An element within a free\-form layout\.

## Syntax<a name="aws-properties-quicksight-dashboard-freeformlayoutelement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-freeformlayoutelement-syntax.json"></a>

```
{
  "[BackgroundStyle](#cfn-quicksight-dashboard-freeformlayoutelement-backgroundstyle)" : FreeFormLayoutElementBackgroundStyle,
  "[BorderStyle](#cfn-quicksight-dashboard-freeformlayoutelement-borderstyle)" : FreeFormLayoutElementBorderStyle,
  "[ElementId](#cfn-quicksight-dashboard-freeformlayoutelement-elementid)" : String,
  "[ElementType](#cfn-quicksight-dashboard-freeformlayoutelement-elementtype)" : String,
  "[Height](#cfn-quicksight-dashboard-freeformlayoutelement-height)" : String,
  "[LoadingAnimation](#cfn-quicksight-dashboard-freeformlayoutelement-loadinganimation)" : LoadingAnimation,
  "[RenderingRules](#cfn-quicksight-dashboard-freeformlayoutelement-renderingrules)" : [ SheetElementRenderingRule, ... ],
  "[SelectedBorderStyle](#cfn-quicksight-dashboard-freeformlayoutelement-selectedborderstyle)" : FreeFormLayoutElementBorderStyle,
  "[Visibility](#cfn-quicksight-dashboard-freeformlayoutelement-visibility)" : String,
  "[Width](#cfn-quicksight-dashboard-freeformlayoutelement-width)" : String,
  "[XAxisLocation](#cfn-quicksight-dashboard-freeformlayoutelement-xaxislocation)" : String,
  "[YAxisLocation](#cfn-quicksight-dashboard-freeformlayoutelement-yaxislocation)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-freeformlayoutelement-syntax.yaml"></a>

```
  [BackgroundStyle](#cfn-quicksight-dashboard-freeformlayoutelement-backgroundstyle): 
    FreeFormLayoutElementBackgroundStyle
  [BorderStyle](#cfn-quicksight-dashboard-freeformlayoutelement-borderstyle): 
    FreeFormLayoutElementBorderStyle
  [ElementId](#cfn-quicksight-dashboard-freeformlayoutelement-elementid): String
  [ElementType](#cfn-quicksight-dashboard-freeformlayoutelement-elementtype): String
  [Height](#cfn-quicksight-dashboard-freeformlayoutelement-height): String
  [LoadingAnimation](#cfn-quicksight-dashboard-freeformlayoutelement-loadinganimation): 
    LoadingAnimation
  [RenderingRules](#cfn-quicksight-dashboard-freeformlayoutelement-renderingrules): 
    - SheetElementRenderingRule
  [SelectedBorderStyle](#cfn-quicksight-dashboard-freeformlayoutelement-selectedborderstyle): 
    FreeFormLayoutElementBorderStyle
  [Visibility](#cfn-quicksight-dashboard-freeformlayoutelement-visibility): String
  [Width](#cfn-quicksight-dashboard-freeformlayoutelement-width): String
  [XAxisLocation](#cfn-quicksight-dashboard-freeformlayoutelement-xaxislocation): String
  [YAxisLocation](#cfn-quicksight-dashboard-freeformlayoutelement-yaxislocation): String
```

## Properties<a name="aws-properties-quicksight-dashboard-freeformlayoutelement-properties"></a>

`BackgroundStyle`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-backgroundstyle"></a>
The background style configuration of a free\-form layout element\.  
*Required*: No  
*Type*: [FreeFormLayoutElementBackgroundStyle](aws-properties-quicksight-dashboard-freeformlayoutelementbackgroundstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BorderStyle`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-borderstyle"></a>
The border style configuration of a free\-form layout element\.  
*Required*: No  
*Type*: [FreeFormLayoutElementBorderStyle](aws-properties-quicksight-dashboard-freeformlayoutelementborderstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElementId`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-elementid"></a>
A unique identifier for an element within a free\-form layout\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElementType`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-elementtype"></a>
The type of element\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FILTER_CONTROL | PARAMETER_CONTROL | TEXT_BOX | VISUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Height`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-height"></a>
The height of an element within a free\-form layout\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadingAnimation`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-loadinganimation"></a>
The loading animation configuration of a free\-form layout element\.  
*Required*: No  
*Type*: [LoadingAnimation](aws-properties-quicksight-dashboard-loadinganimation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RenderingRules`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-renderingrules"></a>
The rendering rules that determine when an element should be displayed within a free\-form layout\.  
*Required*: No  
*Type*: List of [SheetElementRenderingRule](aws-properties-quicksight-dashboard-sheetelementrenderingrule.md)  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedBorderStyle`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-selectedborderstyle"></a>
The border style configuration of a free\-form layout element\. This border style is used when the element is selected\.  
*Required*: No  
*Type*: [FreeFormLayoutElementBorderStyle](aws-properties-quicksight-dashboard-freeformlayoutelementborderstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-visibility"></a>
The visibility of an element within a free\-form layout\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Width`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-width"></a>
The width of an element within a free\-form layout\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisLocation`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-xaxislocation"></a>
The x\-axis coordinate of the element\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxisLocation`  <a name="cfn-quicksight-dashboard-freeformlayoutelement-yaxislocation"></a>
The y\-axis coordinate of the element\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)