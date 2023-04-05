# AWS::QuickSight::Template DateMeasureField<a name="aws-properties-quicksight-template-datemeasurefield"></a>

The measure type field with date type columns\.

## Syntax<a name="aws-properties-quicksight-template-datemeasurefield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-datemeasurefield-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-quicksight-template-datemeasurefield-aggregationfunction)" : String,
  "[Column](#cfn-quicksight-template-datemeasurefield-column)" : ColumnIdentifier,
  "[FieldId](#cfn-quicksight-template-datemeasurefield-fieldid)" : String,
  "[FormatConfiguration](#cfn-quicksight-template-datemeasurefield-formatconfiguration)" : DateTimeFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-template-datemeasurefield-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-quicksight-template-datemeasurefield-aggregationfunction): String
  [Column](#cfn-quicksight-template-datemeasurefield-column): 
    ColumnIdentifier
  [FieldId](#cfn-quicksight-template-datemeasurefield-fieldid): String
  [FormatConfiguration](#cfn-quicksight-template-datemeasurefield-formatconfiguration): 
    DateTimeFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-template-datemeasurefield-properties"></a>

`AggregationFunction`  <a name="cfn-quicksight-template-datemeasurefield-aggregationfunction"></a>
The aggregation function of the measure field\.  
*Required*: No  
*Type*: [String](aws-properties-quicksight-template-aggregationfunction.md)  
*Allowed values*: `COUNT | DISTINCT_COUNT | MAX | MIN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-template-datemeasurefield-column"></a>
The column that is used in the `DateMeasureField`\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-template-datemeasurefield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-template-datemeasurefield-formatconfiguration"></a>
The format configuration of the field\.  
*Required*: No  
*Type*: [DateTimeFormatConfiguration](aws-properties-quicksight-template-datetimeformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)