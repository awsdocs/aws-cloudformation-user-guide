# AWS::QuickSight::Template NumericEqualityFilter<a name="aws-properties-quicksight-template-numericequalityfilter"></a>

A `NumericEqualityFilter` filters values that are equal to the specified value\.

## Syntax<a name="aws-properties-quicksight-template-numericequalityfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-numericequalityfilter-syntax.json"></a>

```
{
  "[AggregationFunction](#cfn-quicksight-template-numericequalityfilter-aggregationfunction)" : AggregationFunction,
  "[Column](#cfn-quicksight-template-numericequalityfilter-column)" : ColumnIdentifier,
  "[FilterId](#cfn-quicksight-template-numericequalityfilter-filterid)" : String,
  "[MatchOperator](#cfn-quicksight-template-numericequalityfilter-matchoperator)" : String,
  "[NullOption](#cfn-quicksight-template-numericequalityfilter-nulloption)" : String,
  "[ParameterName](#cfn-quicksight-template-numericequalityfilter-parametername)" : String,
  "[SelectAllOptions](#cfn-quicksight-template-numericequalityfilter-selectalloptions)" : String,
  "[Value](#cfn-quicksight-template-numericequalityfilter-value)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-numericequalityfilter-syntax.yaml"></a>

```
  [AggregationFunction](#cfn-quicksight-template-numericequalityfilter-aggregationfunction): 
    AggregationFunction
  [Column](#cfn-quicksight-template-numericequalityfilter-column): 
    ColumnIdentifier
  [FilterId](#cfn-quicksight-template-numericequalityfilter-filterid): String
  [MatchOperator](#cfn-quicksight-template-numericequalityfilter-matchoperator): String
  [NullOption](#cfn-quicksight-template-numericequalityfilter-nulloption): String
  [ParameterName](#cfn-quicksight-template-numericequalityfilter-parametername): String
  [SelectAllOptions](#cfn-quicksight-template-numericequalityfilter-selectalloptions): String
  [Value](#cfn-quicksight-template-numericequalityfilter-value): Double
```

## Properties<a name="aws-properties-quicksight-template-numericequalityfilter-properties"></a>

`AggregationFunction`  <a name="cfn-quicksight-template-numericequalityfilter-aggregationfunction"></a>
The aggregation function of the filter\.  
*Required*: No  
*Type*: [AggregationFunction](aws-properties-quicksight-template-aggregationfunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-template-numericequalityfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterId`  <a name="cfn-quicksight-template-numericequalityfilter-filterid"></a>
An identifier that uniquely identifies a filter within a dashboard, analysis, or template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MatchOperator`  <a name="cfn-quicksight-template-numericequalityfilter-matchoperator"></a>
The match operator that is used to determine if a filter should be applied\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DOES_NOT_EQUAL | EQUALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullOption`  <a name="cfn-quicksight-template-numericequalityfilter-nulloption"></a>
This option determines how null values should be treated when filtering data\.  
+  `ALL_VALUES`: Include null values in filtered results\.
+  `NULLS_ONLY`: Only include null values in filtered results\.
+  `NON_NULLS_ONLY`: Exclude null values from filtered results\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL_VALUES | NON_NULLS_ONLY | NULLS_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterName`  <a name="cfn-quicksight-template-numericequalityfilter-parametername"></a>
The parameter whose value should be used for the filter value\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectAllOptions`  <a name="cfn-quicksight-template-numericequalityfilter-selectalloptions"></a>
Select all of the values\. Null is not the assigned value of select all\.  
+  `FILTER_ALL_VALUES` 
*Required*: No  
*Type*: String  
*Allowed values*: `FILTER_ALL_VALUES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-quicksight-template-numericequalityfilter-value"></a>
The input value\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)