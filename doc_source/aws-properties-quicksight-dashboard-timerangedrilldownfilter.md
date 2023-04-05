# AWS::QuickSight::Dashboard TimeRangeDrillDownFilter<a name="aws-properties-quicksight-dashboard-timerangedrilldownfilter"></a>

The time range drill down filter\.

## Syntax<a name="aws-properties-quicksight-dashboard-timerangedrilldownfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-timerangedrilldownfilter-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-dashboard-timerangedrilldownfilter-column)" : ColumnIdentifier,
  "[RangeMaximum](#cfn-quicksight-dashboard-timerangedrilldownfilter-rangemaximum)" : String,
  "[RangeMinimum](#cfn-quicksight-dashboard-timerangedrilldownfilter-rangeminimum)" : String,
  "[TimeGranularity](#cfn-quicksight-dashboard-timerangedrilldownfilter-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-timerangedrilldownfilter-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-dashboard-timerangedrilldownfilter-column): 
    ColumnIdentifier
  [RangeMaximum](#cfn-quicksight-dashboard-timerangedrilldownfilter-rangemaximum): String
  [RangeMinimum](#cfn-quicksight-dashboard-timerangedrilldownfilter-rangeminimum): String
  [TimeGranularity](#cfn-quicksight-dashboard-timerangedrilldownfilter-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-dashboard-timerangedrilldownfilter-properties"></a>

`Column`  <a name="cfn-quicksight-dashboard-timerangedrilldownfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-dashboard-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMaximum`  <a name="cfn-quicksight-dashboard-timerangedrilldownfilter-rangemaximum"></a>
The maximum value for the filter value range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMinimum`  <a name="cfn-quicksight-dashboard-timerangedrilldownfilter-rangeminimum"></a>
The minimum value for the filter value range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-dashboard-timerangedrilldownfilter-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)