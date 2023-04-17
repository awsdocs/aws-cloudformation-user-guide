# AWS::QuickSight::Analysis FilterRelativeDateTimeControl<a name="aws-properties-quicksight-analysis-filterrelativedatetimecontrol"></a>

A control from a date filter that is used to specify the relative date\.

## Syntax<a name="aws-properties-quicksight-analysis-filterrelativedatetimecontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-filterrelativedatetimecontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-analysis-filterrelativedatetimecontrol-displayoptions)" : RelativeDateTimeControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-analysis-filterrelativedatetimecontrol-filtercontrolid)" : String,
  "[SourceFilterId](#cfn-quicksight-analysis-filterrelativedatetimecontrol-sourcefilterid)" : String,
  "[Title](#cfn-quicksight-analysis-filterrelativedatetimecontrol-title)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-filterrelativedatetimecontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-analysis-filterrelativedatetimecontrol-displayoptions): 
    RelativeDateTimeControlDisplayOptions
  [FilterControlId](#cfn-quicksight-analysis-filterrelativedatetimecontrol-filtercontrolid): String
  [SourceFilterId](#cfn-quicksight-analysis-filterrelativedatetimecontrol-sourcefilterid): String
  [Title](#cfn-quicksight-analysis-filterrelativedatetimecontrol-title): String
```

## Properties<a name="aws-properties-quicksight-analysis-filterrelativedatetimecontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-analysis-filterrelativedatetimecontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [RelativeDateTimeControlDisplayOptions](aws-properties-quicksight-analysis-relativedatetimecontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-analysis-filterrelativedatetimecontrol-filtercontrolid"></a>
The ID of the `FilterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-analysis-filterrelativedatetimecontrol-sourcefilterid"></a>
The source filter ID of the `FilterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-filterrelativedatetimecontrol-title"></a>
The title of the `FilterTextAreaControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)