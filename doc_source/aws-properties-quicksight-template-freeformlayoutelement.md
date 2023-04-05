# AWS::QuickSight::Template FreeFormLayoutElement<a name="aws-properties-quicksight-template-freeformlayoutelement"></a>

An element within a free\-form layout\.

## Syntax<a name="aws-properties-quicksight-template-freeformlayoutelement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-freeformlayoutelement-syntax.json"></a>

```
{
  "[BackgroundStyle](#cfn-quicksight-template-freeformlayoutelement-backgroundstyle)" : FreeFormLayoutElementBackgroundStyle,
  "[BorderStyle](#cfn-quicksight-template-freeformlayoutelement-borderstyle)" : FreeFormLayoutElementBorderStyle,
  "[ElementId](#cfn-quicksight-template-freeformlayoutelement-elementid)" : String,
  "[ElementType](#cfn-quicksight-template-freeformlayoutelement-elementtype)" : String,
  "[Height](#cfn-quicksight-template-freeformlayoutelement-height)" : String,
  "[LoadingAnimation](#cfn-quicksight-template-freeformlayoutelement-loadinganimation)" : LoadingAnimation,
  "[RenderingRules](#cfn-quicksight-template-freeformlayoutelement-renderingrules)" : [ SheetElementRenderingRule, ... ],
  "[SelectedBorderStyle](#cfn-quicksight-template-freeformlayoutelement-selectedborderstyle)" : FreeFormLayoutElementBorderStyle,
  "[Visibility](#cfn-quicksight-template-freeformlayoutelement-visibility)" : String,
  "[Width](#cfn-quicksight-template-freeformlayoutelement-width)" : String,
  "[XAxisLocation](#cfn-quicksight-template-freeformlayoutelement-xaxislocation)" : String,
  "[YAxisLocation](#cfn-quicksight-template-freeformlayoutelement-yaxislocation)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-freeformlayoutelement-syntax.yaml"></a>

```
  [BackgroundStyle](#cfn-quicksight-template-freeformlayoutelement-backgroundstyle): 
    FreeFormLayoutElementBackgroundStyle
  [BorderStyle](#cfn-quicksight-template-freeformlayoutelement-borderstyle): 
    FreeFormLayoutElementBorderStyle
  [ElementId](#cfn-quicksight-template-freeformlayoutelement-elementid): String
  [ElementType](#cfn-quicksight-template-freeformlayoutelement-elementtype): String
  [Height](#cfn-quicksight-template-freeformlayoutelement-height): String
  [LoadingAnimation](#cfn-quicksight-template-freeformlayoutelement-loadinganimation): 
    LoadingAnimation
  [RenderingRules](#cfn-quicksight-template-freeformlayoutelement-renderingrules): 
    - SheetElementRenderingRule
  [SelectedBorderStyle](#cfn-quicksight-template-freeformlayoutelement-selectedborderstyle): 
    FreeFormLayoutElementBorderStyle
  [Visibility](#cfn-quicksight-template-freeformlayoutelement-visibility): String
  [Width](#cfn-quicksight-template-freeformlayoutelement-width): String
  [XAxisLocation](#cfn-quicksight-template-freeformlayoutelement-xaxislocation): String
  [YAxisLocation](#cfn-quicksight-template-freeformlayoutelement-yaxislocation): String
```

## Properties<a name="aws-properties-quicksight-template-freeformlayoutelement-properties"></a>

`BackgroundStyle`  <a name="cfn-quicksight-template-freeformlayoutelement-backgroundstyle"></a>
The background style configuration of a free\-form layout element\.  
*Required*: No  
*Type*: [FreeFormLayoutElementBackgroundStyle](aws-properties-quicksight-template-freeformlayoutelementbackgroundstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BorderStyle`  <a name="cfn-quicksight-template-freeformlayoutelement-borderstyle"></a>
The border style configuration of a free\-form layout element\.  
*Required*: No  
*Type*: [FreeFormLayoutElementBorderStyle](aws-properties-quicksight-template-freeformlayoutelementborderstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElementId`  <a name="cfn-quicksight-template-freeformlayoutelement-elementid"></a>
A unique identifier for an element within a free\-form layout\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ElementType`  <a name="cfn-quicksight-template-freeformlayoutelement-elementtype"></a>
The type of element\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FILTER_CONTROL | PARAMETER_CONTROL | TEXT_BOX | VISUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Height`  <a name="cfn-quicksight-template-freeformlayoutelement-height"></a>
The height of an element within a free\-form layout\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadingAnimation`  <a name="cfn-quicksight-template-freeformlayoutelement-loadinganimation"></a>
The loading animation configuration of a free\-form layout element\.  
*Required*: No  
*Type*: [LoadingAnimation](aws-properties-quicksight-template-loadinganimation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RenderingRules`  <a name="cfn-quicksight-template-freeformlayoutelement-renderingrules"></a>
The rendering rules that determine when an element should be displayed within a free\-form layout\.  
*Required*: No  
*Type*: List of [SheetElementRenderingRule](aws-properties-quicksight-template-sheetelementrenderingrule.md)  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedBorderStyle`  <a name="cfn-quicksight-template-freeformlayoutelement-selectedborderstyle"></a>
The border style configuration of a free\-form layout element\. This border style is used when the element is selected\.  
*Required*: No  
*Type*: [FreeFormLayoutElementBorderStyle](aws-properties-quicksight-template-freeformlayoutelementborderstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Visibility`  <a name="cfn-quicksight-template-freeformlayoutelement-visibility"></a>
The visibility of an element within a free\-form layout\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HIDDEN | VISIBLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Width`  <a name="cfn-quicksight-template-freeformlayoutelement-width"></a>
The width of an element within a free\-form layout\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XAxisLocation`  <a name="cfn-quicksight-template-freeformlayoutelement-xaxislocation"></a>
The x\-axis coordinate of the element\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`YAxisLocation`  <a name="cfn-quicksight-template-freeformlayoutelement-yaxislocation"></a>
The y\-axis coordinate of the element\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)