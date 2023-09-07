# AWS::QuickSight::Analysis SliderControlDisplayOptions<a name="aws-properties-quicksight-analysis-slidercontroldisplayoptions"></a>

The display options of a control\.

## Syntax<a name="aws-properties-quicksight-analysis-slidercontroldisplayoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-slidercontroldisplayoptions-syntax.json"></a>

```
{
  "[InfoIconLabelOptions](#cfn-quicksight-analysis-slidercontroldisplayoptions-infoiconlabeloptions)" : SheetControlInfoIconLabelOptions,
  "[TitleOptions](#cfn-quicksight-analysis-slidercontroldisplayoptions-titleoptions)" : LabelOptions
}
```

### YAML<a name="aws-properties-quicksight-analysis-slidercontroldisplayoptions-syntax.yaml"></a>

```
  [InfoIconLabelOptions](#cfn-quicksight-analysis-slidercontroldisplayoptions-infoiconlabeloptions): 
    SheetControlInfoIconLabelOptions
  [TitleOptions](#cfn-quicksight-analysis-slidercontroldisplayoptions-titleoptions): 
    LabelOptions
```

## Properties<a name="aws-properties-quicksight-analysis-slidercontroldisplayoptions-properties"></a>

`InfoIconLabelOptions`  <a name="cfn-quicksight-analysis-slidercontroldisplayoptions-infoiconlabeloptions"></a>
The configuration of info icon label options\.  
*Required*: No  
*Type*: [SheetControlInfoIconLabelOptions](aws-properties-quicksight-analysis-sheetcontrolinfoiconlabeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TitleOptions`  <a name="cfn-quicksight-analysis-slidercontroldisplayoptions-titleoptions"></a>
The options to configure the title visibility, name, and font size\.  
*Required*: No  
*Type*: [LabelOptions](aws-properties-quicksight-analysis-labeloptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)