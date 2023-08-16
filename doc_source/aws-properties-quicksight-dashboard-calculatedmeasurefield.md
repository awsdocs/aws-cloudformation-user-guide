# AWS::QuickSight::Dashboard CalculatedMeasureField<a name="aws-properties-quicksight-dashboard-calculatedmeasurefield"></a>

The table calculation measure field for pivot tables\.

## Syntax<a name="aws-properties-quicksight-dashboard-calculatedmeasurefield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-calculatedmeasurefield-syntax.json"></a>

```
{
  "[Expression](#cfn-quicksight-dashboard-calculatedmeasurefield-expression)" : String,
  "[FieldId](#cfn-quicksight-dashboard-calculatedmeasurefield-fieldid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-calculatedmeasurefield-syntax.yaml"></a>

```
  [Expression](#cfn-quicksight-dashboard-calculatedmeasurefield-expression): String
  [FieldId](#cfn-quicksight-dashboard-calculatedmeasurefield-fieldid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-calculatedmeasurefield-properties"></a>

`Expression`  <a name="cfn-quicksight-dashboard-calculatedmeasurefield-expression"></a>
The expression in the table calculation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-dashboard-calculatedmeasurefield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)