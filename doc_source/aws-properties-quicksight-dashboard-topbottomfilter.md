# AWS::QuickSight::Dashboard TopBottomFilter<a name="aws-properties-quicksight-dashboard-topbottomfilter"></a>

A `TopBottomFilter` filters values that are at the top or the bottom\.

## Syntax<a name="aws-properties-quicksight-dashboard-topbottomfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-topbottomfilter-syntax.json"></a>

```
{
  "[AggregationSortConfigurations](#cfn-quicksight-dashboard-topbottomfilter-aggregationsortconfigurations)" : [ AggregationSortConfiguration, ... ],
  "[Column](#cfn-quicksight-dashboard-topbottomfilter-column)" : ColumnIdentifier,
  "[FilterId](#cfn-quicksight-dashboard-topbottomfilter-filterid)" : String,
  "[Limit](#cfn-quicksight-dashboard-topbottomfilter-limit)" : Double,
  "[ParameterName](#cfn-quicksight-dashboard-topbottomfilter-parametername)" : String,
  "[TimeGranularity](#cfn-quicksight-dashboard-topbottomfilter-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-topbottomfilter-syntax.yaml"></a>

```
  [AggregationSortConfigurations](#cfn-quicksight-dashboard-topbottomfilter-aggregationsortconfigurations): 
    - AggregationSortConfiguration
  [Column](#cfn-quicksight-dashboard-topbottomfilter-column): 
    ColumnIdentifier
  [FilterId](#cfn-quicksight-dashboard-topbottomfilter-filterid): String
  [Limit](#cfn-quicksight-dashboard-topbottomfilter-limit): Double
  [ParameterName](#cfn-quicksight-dashboard-topbottomfilter-parametername): String
  [TimeGranularity](#cfn-quicksight-dashboard-topbottomfilter-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-dashboard-topbottomfilter-properties"></a>

`AggregationSortConfigurations`  <a name="cfn-quicksight-dashboard-topbottomfilter-aggregationsortconfigurations"></a>
The aggregation and sort configuration of the top bottom filter\.  
*Required*: Yes  
*Type*: List of [AggregationSortConfiguration](aws-properties-quicksight-dashboard-aggregationsortconfiguration.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-dashboard-topbottomfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterId`  <a name="cfn-quicksight-dashboard-topbottomfilter-filterid"></a>
An identifier that uniquely identifies a filter within a dashboard, analysis, or template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limit`  <a name="cfn-quicksight-dashboard-topbottomfilter-limit"></a>
The number of items to include in the top bottom filter results\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterName`  <a name="cfn-quicksight-dashboard-topbottomfilter-parametername"></a>
The parameter whose value should be used for the filter value\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-dashboard-topbottomfilter-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)