# AWS::QuickSight::Dashboard FilterSliderControl<a name="aws-properties-quicksight-dashboard-filterslidercontrol"></a>

A control to display a horizontal toggle bar\. This is used to change a value by sliding the toggle\.

## Syntax<a name="aws-properties-quicksight-dashboard-filterslidercontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filterslidercontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-dashboard-filterslidercontrol-displayoptions)" : SliderControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-dashboard-filterslidercontrol-filtercontrolid)" : String,
  "[MaximumValue](#cfn-quicksight-dashboard-filterslidercontrol-maximumvalue)" : Double,
  "[MinimumValue](#cfn-quicksight-dashboard-filterslidercontrol-minimumvalue)" : Double,
  "[SourceFilterId](#cfn-quicksight-dashboard-filterslidercontrol-sourcefilterid)" : String,
  "[StepSize](#cfn-quicksight-dashboard-filterslidercontrol-stepsize)" : Double,
  "[Title](#cfn-quicksight-dashboard-filterslidercontrol-title)" : String,
  "[Type](#cfn-quicksight-dashboard-filterslidercontrol-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filterslidercontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-dashboard-filterslidercontrol-displayoptions): 
    SliderControlDisplayOptions
  [FilterControlId](#cfn-quicksight-dashboard-filterslidercontrol-filtercontrolid): String
  [MaximumValue](#cfn-quicksight-dashboard-filterslidercontrol-maximumvalue): Double
  [MinimumValue](#cfn-quicksight-dashboard-filterslidercontrol-minimumvalue): Double
  [SourceFilterId](#cfn-quicksight-dashboard-filterslidercontrol-sourcefilterid): String
  [StepSize](#cfn-quicksight-dashboard-filterslidercontrol-stepsize): Double
  [Title](#cfn-quicksight-dashboard-filterslidercontrol-title): String
  [Type](#cfn-quicksight-dashboard-filterslidercontrol-type): String
```

## Properties<a name="aws-properties-quicksight-dashboard-filterslidercontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-dashboard-filterslidercontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [SliderControlDisplayOptions](aws-properties-quicksight-dashboard-slidercontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-dashboard-filterslidercontrol-filtercontrolid"></a>
The ID of the `FilterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumValue`  <a name="cfn-quicksight-dashboard-filterslidercontrol-maximumvalue"></a>
The smaller value that is displayed at the left of the slider\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumValue`  <a name="cfn-quicksight-dashboard-filterslidercontrol-minimumvalue"></a>
The larger value that is displayed at the right of the slider\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-dashboard-filterslidercontrol-sourcefilterid"></a>
The source filter ID of the `FilterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepSize`  <a name="cfn-quicksight-dashboard-filterslidercontrol-stepsize"></a>
The number of increments that the slider bar is divided into\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-filterslidercontrol-title"></a>
The title of the `FilterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-filterslidercontrol-type"></a>
The type of `FilterSliderControl`\. Choose one of the following options:  
+  `SINGLE_POINT`: Filter against\(equals\) a single data point\.
+  `RANGE`: Filter data that is in a specified range\.
*Required*: No  
*Type*: String  
*Allowed values*: `RANGE | SINGLE_POINT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)