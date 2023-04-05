# AWS::QuickSight::Dashboard FilterDateTimePickerControl<a name="aws-properties-quicksight-dashboard-filterdatetimepickercontrol"></a>

A control from a date filter that is used to specify date and time\.

## Syntax<a name="aws-properties-quicksight-dashboard-filterdatetimepickercontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-filterdatetimepickercontrol-syntax.json"></a>

```
{
  "[DisplayOptions](#cfn-quicksight-dashboard-filterdatetimepickercontrol-displayoptions)" : DateTimePickerControlDisplayOptions,
  "[FilterControlId](#cfn-quicksight-dashboard-filterdatetimepickercontrol-filtercontrolid)" : String,
  "[SourceFilterId](#cfn-quicksight-dashboard-filterdatetimepickercontrol-sourcefilterid)" : String,
  "[Title](#cfn-quicksight-dashboard-filterdatetimepickercontrol-title)" : String,
  "[Type](#cfn-quicksight-dashboard-filterdatetimepickercontrol-type)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-filterdatetimepickercontrol-syntax.yaml"></a>

```
  [DisplayOptions](#cfn-quicksight-dashboard-filterdatetimepickercontrol-displayoptions): 
    DateTimePickerControlDisplayOptions
  [FilterControlId](#cfn-quicksight-dashboard-filterdatetimepickercontrol-filtercontrolid): String
  [SourceFilterId](#cfn-quicksight-dashboard-filterdatetimepickercontrol-sourcefilterid): String
  [Title](#cfn-quicksight-dashboard-filterdatetimepickercontrol-title): String
  [Type](#cfn-quicksight-dashboard-filterdatetimepickercontrol-type): String
```

## Properties<a name="aws-properties-quicksight-dashboard-filterdatetimepickercontrol-properties"></a>

`DisplayOptions`  <a name="cfn-quicksight-dashboard-filterdatetimepickercontrol-displayoptions"></a>
The display options of a control\.  
*Required*: No  
*Type*: [DateTimePickerControlDisplayOptions](aws-properties-quicksight-dashboard-datetimepickercontroldisplayoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterControlId`  <a name="cfn-quicksight-dashboard-filterdatetimepickercontrol-filtercontrolid"></a>
The ID of the `FilterDateTimePickerControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceFilterId`  <a name="cfn-quicksight-dashboard-filterdatetimepickercontrol-sourcefilterid"></a>
The source filter ID of the `FilterDateTimePickerControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-quicksight-dashboard-filterdatetimepickercontrol-title"></a>
The title of the `FilterDateTimePickerControl`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-quicksight-dashboard-filterdatetimepickercontrol-type"></a>
The date time picker type of a `FilterDateTimePickerControl`\. Choose one of the following options:  
+  `SINGLE_VALUED`: The filter condition is a fixed date\.
+  `DATE_RANGE`: The filter condition is a date time range\.
*Required*: No  
*Type*: String  
*Allowed values*: `DATE_RANGE | SINGLE_VALUED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)