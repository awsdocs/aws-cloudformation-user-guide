# AWS::QuickSight::Template FilterSliderControl<a name="aws-properties-quicksight-template-filterslidercontrol"></a>

A control to display a horizontal toggle bar\. This is used to change a value by sliding the toggle\.

## Syntax<a name="aws-properties-quicksight-template-filterslidercontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-filterslidercontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-template-filterslidercontrol-displayoptions)" : SliderControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-template-filterslidercontrol-filtercontrolid)" : String,
  "[MaximumValue](#cfn-quicksight-template-filterslidercontrol-maximumvalue)" : Double,
  "[MinimumValue](#cfn-quicksight-template-filterslidercontrol-minimumvalue)" : Double,
  "[SourceFilterId](#cfn-quicksight-template-filterslidercontrol-sourcefilterid)" : String,
  "[StepSize](#cfn-quicksight-template-filterslidercontrol-stepsize)" : Double,
  "[Title](#cfn-quicksight-template-filterslidercontrol-title)" : String,
  "[Type](#cfn-quicksight-template-filterslidercontrol-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-filterslidercontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-template-filterslidercontrol-displayoptions): 
    SliderControlDisplayOptions
  [FilterControlId](#cfn-quicksight-template-filterslidercontrol-filtercontrolid): String
  [MaximumValue](#cfn-quicksight-template-filterslidercontrol-maximumvalue): Double
  [MinimumValue](#cfn-quicksight-template-filterslidercontrol-minimumvalue): Double
  [SourceFilterId](#cfn-quicksight-template-filterslidercontrol-sourcefilterid): String
  [StepSize](#cfn-quicksight-template-filterslidercontrol-stepsize): Double
  [Title](#cfn-quicksight-template-filterslidercontrol-title): String
  [Type](#cfn-quicksight-template-filterslidercontrol-type): String
```

## Properties<a name="aws-properties-quicksight-template-filterslidercontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-template-filterslidercontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [SliderControlDisplayOptions](aws-properties-quicksight-template-slidercontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-template-filterslidercontrol-filtercontrolid"></a>
The ID of the `FilterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumValue`  <a name="cfn-quicksight-template-filterslidercontrol-maximumvalue"></a>
The smaller value that is displayed at the left of the slider\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumValue`  <a name="cfn-quicksight-template-filterslidercontrol-minimumvalue"></a>
The larger value that is displayed at the right of the slider\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-template-filterslidercontrol-sourcefilterid"></a>
The source filter ID of the `FilterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepSize`  <a name="cfn-quicksight-template-filterslidercontrol-stepsize"></a>
The number of increments that the slider bar is divided into\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-template-filterslidercontrol-title"></a>
The title of the `FilterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-template-filterslidercontrol-type"></a>
The type of `FilterSliderControl`\. Choose one of the following options:  
+  `SINGLE_POINT`: Filter against\(equals\) a single data point\.
+  `RANGE`: Filter data that is in a specified range\.
*Required*: No  
*Type*: String  
*Allowed values*: `RANGE | SINGLE_POINT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)