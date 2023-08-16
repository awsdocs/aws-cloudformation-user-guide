# AWS::QuickSight::Analysis FilterDateTimePickerControl<a name="aws-properties-quicksight-analysis-filterdatetimepickercontrol"></a>

A control from a date filter that is used to specify date and time\.

## Syntax<a name="aws-properties-quicksight-analysis-filterdatetimepickercontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-filterdatetimepickercontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-analysis-filterdatetimepickercontrol-displayoptions)" : DateTimePickerControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-analysis-filterdatetimepickercontrol-filtercontrolid)" : String,
  "[SourceFilterId](#cfn-quicksight-analysis-filterdatetimepickercontrol-sourcefilterid)" : String,
  "[Title](#cfn-quicksight-analysis-filterdatetimepickercontrol-title)" : String,
  "[Type](#cfn-quicksight-analysis-filterdatetimepickercontrol-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-filterdatetimepickercontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-analysis-filterdatetimepickercontrol-displayoptions): 
    DateTimePickerControlDisplayOptions
  [FilterControlId](#cfn-quicksight-analysis-filterdatetimepickercontrol-filtercontrolid): String
  [SourceFilterId](#cfn-quicksight-analysis-filterdatetimepickercontrol-sourcefilterid): String
  [Title](#cfn-quicksight-analysis-filterdatetimepickercontrol-title): String
  [Type](#cfn-quicksight-analysis-filterdatetimepickercontrol-type): String
```

## Properties<a name="aws-properties-quicksight-analysis-filterdatetimepickercontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-analysis-filterdatetimepickercontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [DateTimePickerControlDisplayOptions](aws-properties-quicksight-analysis-datetimepickercontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-analysis-filterdatetimepickercontrol-filtercontrolid"></a>
The ID of the `FilterDateTimePickerControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-analysis-filterdatetimepickercontrol-sourcefilterid"></a>
The source filter ID of the `FilterDateTimePickerControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-analysis-filterdatetimepickercontrol-title"></a>
The title of the `FilterDateTimePickerControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-analysis-filterdatetimepickercontrol-type"></a>
The date time picker type of a `FilterDateTimePickerControl`\. Choose one of the following options:  
+  `SINGLE_VALUED`: The filter condition is a fixed date\.
+  `DATE_RANGE`: The filter condition is a date time range\.
*Required*: No  
*Type*: String  
*Allowed values*: `DATE_RANGE | SINGLE_VALUED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)