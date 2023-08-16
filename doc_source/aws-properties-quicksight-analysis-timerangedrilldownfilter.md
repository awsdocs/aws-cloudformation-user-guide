# AWS::QuickSight::Analysis TimeRangeDrillDownFilter<a name="aws-properties-quicksight-analysis-timerangedrilldownfilter"></a>

The time range drill down filter\.

## Syntax<a name="aws-properties-quicksight-analysis-timerangedrilldownfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-timerangedrilldownfilter-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-analysis-timerangedrilldownfilter-column)" : ColumnIdentifier,
  "[RangeMaximum](#cfn-quicksight-analysis-timerangedrilldownfilter-rangemaximum)" : String,
  "[RangeMinimum](#cfn-quicksight-analysis-timerangedrilldownfilter-rangeminimum)" : String,
  "[TimeGranularity](#cfn-quicksight-analysis-timerangedrilldownfilter-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-timerangedrilldownfilter-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-analysis-timerangedrilldownfilter-column): 
    ColumnIdentifier
  [RangeMaximum](#cfn-quicksight-analysis-timerangedrilldownfilter-rangemaximum): String
  [RangeMinimum](#cfn-quicksight-analysis-timerangedrilldownfilter-rangeminimum): String
  [TimeGranularity](#cfn-quicksight-analysis-timerangedrilldownfilter-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-analysis-timerangedrilldownfilter-properties"></a>

`Column`  <a name="cfn-quicksight-analysis-timerangedrilldownfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-analysis-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMaximum`  <a name="cfn-quicksight-analysis-timerangedrilldownfilter-rangemaximum"></a>
The maximum value for the filter value range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMinimum`  <a name="cfn-quicksight-analysis-timerangedrilldownfilter-rangeminimum"></a>
The minimum value for the filter value range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-analysis-timerangedrilldownfilter-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)