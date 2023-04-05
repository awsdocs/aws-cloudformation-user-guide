# AWS::QuickSight::Analysis NumericalMeasureField<a name="aws-properties-quicksight-analysis-numericalmeasurefield"></a>

The measure type field with numerical type columns\.

## Syntax<a name="aws-properties-quicksight-analysis-numericalmeasurefield-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-numericalmeasurefield-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-quicksight-analysis-numericalmeasurefield-aggregationfunction)" : NumericalAggregationFunction,
  "[Column](#cfn-quicksight-analysis-numericalmeasurefield-column)" : ColumnIdentifier,
  "[FieldId](#cfn-quicksight-analysis-numericalmeasurefield-fieldid)" : String,
  "[FormatConfiguration](#cfn-quicksight-analysis-numericalmeasurefield-formatconfiguration)" : NumberFormatConfiguration
}
```

### YAML<a name="aws-properties-quicksight-analysis-numericalmeasurefield-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-quicksight-analysis-numericalmeasurefield-aggregationfunction): 
    NumericalAggregationFunction
  [Column](#cfn-quicksight-analysis-numericalmeasurefield-column): 
    ColumnIdentifier
  [FieldId](#cfn-quicksight-analysis-numericalmeasurefield-fieldid): String
  [FormatConfiguration](#cfn-quicksight-analysis-numericalmeasurefield-formatconfiguration): 
    NumberFormatConfiguration
```

## Properties<a name="aws-properties-quicksight-analysis-numericalmeasurefield-properties"></a>

`AggregationFunction`  <a name="cfn-quicksight-analysis-numericalmeasurefield-aggregationfunction"></a>
The aggregation function of the measure field\.  
*Required*: No  
*Type*: [NumericalAggregationFunction](aws-properties-quicksight-analysis-numericalaggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-analysis-numericalmeasurefield-column"></a>
The column that is used in the `NumericalMeasureField`\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-analysis-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-analysis-numericalmeasurefield-fieldid"></a>
The custom field ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FormatConfiguration`  <a name="cfn-quicksight-analysis-numericalmeasurefield-formatconfiguration"></a>
The format configuration of the field\.  
*Required*: No  
*Type*: [NumberFormatConfiguration](aws-properties-quicksight-analysis-numberformatconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)