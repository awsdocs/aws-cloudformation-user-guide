# AWS::QuickSight::Dashboard NumericalMeasureField<a name="aws-properties-quicksight-dashboard-numericalmeasurefield"></a>

The measure type field with numerical type columns\.

## Syntax<a name="aws-properties-quicksight-dashboard-numericalmeasurefield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-numericalmeasurefield-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-quicksight-dashboard-numericalmeasurefield-aggregationfunction)" : NumericalAggregationFunction,
  "[Column](#cfn-quicksight-dashboard-numericalmeasurefield-column)" : ColumnIdentifier,
  "[FieldId](#cfn-quicksight-dashboard-numericalmeasurefield-fieldid)" : String,
  "[FormatConfiguration](#cfn-quicksight-dashboard-numericalmeasurefield-formatconfiguration)" : NumberFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-numericalmeasurefield-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-quicksight-dashboard-numericalmeasurefield-aggregationfunction): 
    NumericalAggregationFunction
  [Column](#cfn-quicksight-dashboard-numericalmeasurefield-column): 
    ColumnIdentifier
  [FieldId](#cfn-quicksight-dashboard-numericalmeasurefield-fieldid): String
  [FormatConfiguration](#cfn-quicksight-dashboard-numericalmeasurefield-formatconfiguration): 
    NumberFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-numericalmeasurefield-properties"></a>

`AggregationFunction`  <a name="cfn-quicksight-dashboard-numericalmeasurefield-aggregationfunction"></a>
The aggregation function of the measure field\.  
*Required*: No  
*Type*: [NumericalAggregationFunction](aws-properties-quicksight-dashboard-numericalaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-dashboard-numericalmeasurefield-column"></a>
The column that is used in the `NumericalMeasureField`\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-dashboard-numericalmeasurefield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-dashboard-numericalmeasurefield-formatconfiguration"></a>
The format configuration of the field\.  
*Required*: No  
*Type*: [NumberFormatConfiguration](aws-properties-quicksight-dashboard-numberformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)