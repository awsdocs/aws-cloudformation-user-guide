# AWS::QuickSight::Template RelativeDatesFilter<a name="aws-properties-quicksight-template-relativedatesfilter"></a>

A `RelativeDatesFilter` filters relative dates values\.

## Syntax<a name="aws-properties-quicksight-template-relativedatesfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-relativedatesfilter-syntax.json"></a>

```
{
  "[AnchorDateConfiguration](#cfn-quicksight-template-relativedatesfilter-anchordateconfiguration)" : AnchorDateConfiguration,
  "[Column](#cfn-quicksight-template-relativedatesfilter-column)" : ColumnIdentifier,
  "[ExcludePeriodConfiguration](#cfn-quicksight-template-relativedatesfilter-excludeperiodconfiguration)" : ExcludePeriodConfiguration,
  "[FilterId](#cfn-quicksight-template-relativedatesfilter-filterid)" : String,
  "[MinimumGranularity](#cfn-quicksight-template-relativedatesfilter-minimumgranularity)" : String,
  "[NullOption](#cfn-quicksight-template-relativedatesfilter-nulloption)" : String,
  "[ParameterName](#cfn-quicksight-template-relativedatesfilter-parametername)" : String,
  "[RelativeDateType](#cfn-quicksight-template-relativedatesfilter-relativedatetype)" : String,
  "[RelativeDateValue](#cfn-quicksight-template-relativedatesfilter-relativedatevalue)" : Double,
  "[TimeGranularity](#cfn-quicksight-template-relativedatesfilter-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-relativedatesfilter-syntax.yaml"></a>

```
  [AnchorDateConfiguration](#cfn-quicksight-template-relativedatesfilter-anchordateconfiguration): 
    AnchorDateConfiguration
  [Column](#cfn-quicksight-template-relativedatesfilter-column): 
    ColumnIdentifier
  [ExcludePeriodConfiguration](#cfn-quicksight-template-relativedatesfilter-excludeperiodconfiguration): 
    ExcludePeriodConfiguration
  [FilterId](#cfn-quicksight-template-relativedatesfilter-filterid): String
  [MinimumGranularity](#cfn-quicksight-template-relativedatesfilter-minimumgranularity): String
  [NullOption](#cfn-quicksight-template-relativedatesfilter-nulloption): String
  [ParameterName](#cfn-quicksight-template-relativedatesfilter-parametername): String
  [RelativeDateType](#cfn-quicksight-template-relativedatesfilter-relativedatetype): String
  [RelativeDateValue](#cfn-quicksight-template-relativedatesfilter-relativedatevalue): Double
  [TimeGranularity](#cfn-quicksight-template-relativedatesfilter-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-template-relativedatesfilter-properties"></a>

`AnchorDateConfiguration`  <a name="cfn-quicksight-template-relativedatesfilter-anchordateconfiguration"></a>
The date configuration of the filter\.  
*Required*: Yes  
*Type*: [AnchorDateConfiguration](aws-properties-quicksight-template-anchordateconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Column`  <a name="cfn-quicksight-template-relativedatesfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludePeriodConfiguration`  <a name="cfn-quicksight-template-relativedatesfilter-excludeperiodconfiguration"></a>
The configuration for the exclude period of the filter\.  
*Required*: No  
*Type*: [ExcludePeriodConfiguration](aws-properties-quicksight-template-excludeperiodconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterId`  <a name="cfn-quicksight-template-relativedatesfilter-filterid"></a>
An identifier that uniquely identifies a filter within a dashboard, analysis, or template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumGranularity`  <a name="cfn-quicksight-template-relativedatesfilter-minimumgranularity"></a>
The minimum granularity \(period granularity\) of the relative dates filter\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NullOption`  <a name="cfn-quicksight-template-relativedatesfilter-nulloption"></a>
This option determines how null values should be treated when filtering data\.  
+  `ALL_VALUES`: Include null values in filtered results\.
+  `NULLS_ONLY`: Only include null values in filtered results\.
+  `NON_NULLS_ONLY`: Exclude null values from filtered results\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALL_VALUES | NON_NULLS_ONLY | NULLS_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterName`  <a name="cfn-quicksight-template-relativedatesfilter-parametername"></a>
The parameter whose value should be used for the filter value\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[a-zA-Z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelativeDateType`  <a name="cfn-quicksight-template-relativedatesfilter-relativedatetype"></a>
The range date type of the filter\. Choose one of the options below:  
+  `PREVIOUS` 
+  `THIS` 
+  `LAST` 
+  `NOW` 
+  `NEXT` 
*Required*: Yes  
*Type*: String  
*Allowed values*: `LAST | NEXT | NOW | PREVIOUS | THIS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelativeDateValue`  <a name="cfn-quicksight-template-relativedatesfilter-relativedatevalue"></a>
The date value of the filter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-template-relativedatesfilter-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)