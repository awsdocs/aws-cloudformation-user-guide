# AWS::QuickSight::Analysis ParameterSliderControl<a name="aws-properties-quicksight-analysis-parameterslidercontrol"></a>

A control to display a horizontal toggle bar\. This is used to change a value by sliding the toggle\.

## Syntax<a name="aws-properties-quicksight-analysis-parameterslidercontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-parameterslidercontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-analysis-parameterslidercontrol-displayoptions)" : SliderControlDisplayOptions,
  "[MaximumValue](#cfn-quicksight-analysis-parameterslidercontrol-maximumvalue)" : Double,
  "[MinimumValue](#cfn-quicksight-analysis-parameterslidercontrol-minimumvalue)" : Double,
  "[ParameterControlId](#cfn-quicksight-analysis-parameterslidercontrol-parametercontrolid)" : String,
  "[SourceParameterName](#cfn-quicksight-analysis-parameterslidercontrol-sourceparametername)" : String,
  "[StepSize](#cfn-quicksight-analysis-parameterslidercontrol-stepsize)" : Double,
  "[Title](#cfn-quicksight-analysis-parameterslidercontrol-title)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-parameterslidercontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-analysis-parameterslidercontrol-displayoptions): 
    SliderControlDisplayOptions
  [MaximumValue](#cfn-quicksight-analysis-parameterslidercontrol-maximumvalue): Double
  [MinimumValue](#cfn-quicksight-analysis-parameterslidercontrol-minimumvalue): Double
  [ParameterControlId](#cfn-quicksight-analysis-parameterslidercontrol-parametercontrolid): String
  [SourceParameterName](#cfn-quicksight-analysis-parameterslidercontrol-sourceparametername): String
  [StepSize](#cfn-quicksight-analysis-parameterslidercontrol-stepsize): Double
  [Title](#cfn-quicksight-analysis-parameterslidercontrol-title): String
```

## Properties<a name="aws-properties-quicksight-analysis-parameterslidercontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-analysis-parameterslidercontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [SliderControlDisplayOptions](aws-properties-quicksight-analysis-slidercontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumValue`  <a name="cfn-quicksight-analysis-parameterslidercontrol-maximumvalue"></a>
The smaller value that is displayed at the left of the slider\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumValue`  <a name="cfn-quicksight-analysis-parameterslidercontrol-minimumvalue"></a>
The larger value that is displayed at the right of the slider\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterControlId`  <a name="cfn-quicksight-analysis-parameterslidercontrol-parametercontrolid"></a>
The ID of the `ParameterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceParameterName`  <a name="cfn-quicksight-analysis-parameterslidercontrol-sourceparametername"></a>
The source parameter name of the `ParameterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepSize`  <a name="cfn-quicksight-analysis-parameterslidercontrol-stepsize"></a>
The number of increments that the slider bar is divided into\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-parameterslidercontrol-title"></a>
The title of the `ParameterSliderControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)