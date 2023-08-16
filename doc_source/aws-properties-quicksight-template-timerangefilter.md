# AWS::QuickSight::Template TimeRangeFilter<a name="aws-properties-quicksight-template-timerangefilter"></a>

A `TimeRangeFilter` filters values that are between two specified values\.

## Syntax<a name="aws-properties-quicksight-template-timerangefilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-timerangefilter-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-template-timerangefilter-column)" : ColumnIdentifier,
  "[ExcludePeriodConfiguration](#cfn-quicksight-template-timerangefilter-excludeperiodconfiguration)" : ExcludePeriodConfiguration,
  "[FilterId](#cfn-quicksight-template-timerangefilter-filterid)" : String,
  "[IncludeMaximum](#cfn-quicksight-template-timerangefilter-includemaximum)" : Boolean,
  "[IncludeMinimum](#cfn-quicksight-template-timerangefilter-includeminimum)" : Boolean,
  "[NullOption](#cfn-quicksight-template-timerangefilter-nulloption)" : String,
  "[RangeMaximumValue](#cfn-quicksight-template-timerangefilter-rangemaximumvalue)" : TimeRangeFilterValue,
  "[RangeMinimumValue](#cfn-quicksight-template-timerangefilter-rangeminimumvalue)" : TimeRangeFilterValue,
  "[TimeGranularity](#cfn-quicksight-template-timerangefilter-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-timerangefilter-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-template-timerangefilter-column): 
    ColumnIdentifier
  [ExcludePeriodConfiguration](#cfn-quicksight-template-timerangefilter-excludeperiodconfiguration): 
    ExcludePeriodConfiguration
  [FilterId](#cfn-quicksight-template-timerangefilter-filterid): String
  [IncludeMaximum](#cfn-quicksight-template-timerangefilter-includemaximum): Boolean
  [IncludeMinimum](#cfn-quicksight-template-timerangefilter-includeminimum): Boolean
  [NullOption](#cfn-quicksight-template-timerangefilter-nulloption): String
  [RangeMaximumValue](#cfn-quicksight-template-timerangefilter-rangemaximumvalue): 
    TimeRangeFilterValue
  [RangeMinimumValue](#cfn-quicksight-template-timerangefilter-rangeminimumvalue): 
    TimeRangeFilterValue
  [TimeGranularity](#cfn-quicksight-template-timerangefilter-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-template-timerangefilter-properties"></a>

`Column`  <a name="cfn-quicksight-template-timerangefilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludePeriodConfiguration`  <a name="cfn-quicksight-template-timerangefilter-excludeperiodconfiguration"></a>
The exclude period of the time range filter\.  
*Required*: No  
*Type*: [ExcludePeriodConfiguration](aws-properties-quicksight-template-excludeperiodconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterId`  <a name="cfn-quicksight-template-timerangefilter-filterid"></a>
An identifier that uniquely identifies a filter within a dashboard, analysis, or template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeMaximum`  <a name="cfn-quicksight-template-timerangefilter-includemaximum"></a>
Determines whether the maximum value in the filter value range should be included in the filtered results\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeMinimum`  <a name="cfn-quicksight-template-timerangefilter-includeminimum"></a>
Determines whether the minimum value in the filter value range should be included in the filtered results\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullOption`  <a name="cfn-quicksight-template-timerangefilter-nulloption"></a>
This option determines how null values should be treated when filtering data\.  
+  `ALL_VALUES`: Include null values in filtered results\.
+  `NULLS_ONLY`: Only include null values in filtered results\.
+  `NON_NULLS_ONLY`: Exclude null values from filtered results\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL_VALUES | NON_NULLS_ONLY | NULLS_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMaximumValue`  <a name="cfn-quicksight-template-timerangefilter-rangemaximumvalue"></a>
The maximum value for the filter value range\.  
*Required*: No  
*Type*: [TimeRangeFilterValue](aws-properties-quicksight-template-timerangefiltervalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMinimumValue`  <a name="cfn-quicksight-template-timerangefilter-rangeminimumvalue"></a>
The minimum value for the filter value range\.  
*Required*: No  
*Type*: [TimeRangeFilterValue](aws-properties-quicksight-template-timerangefiltervalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-template-timerangefilter-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)