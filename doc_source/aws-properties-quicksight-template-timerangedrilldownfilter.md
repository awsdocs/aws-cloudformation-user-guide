# AWS::QuickSight::Template TimeRangeDrillDownFilter<a name="aws-properties-quicksight-template-timerangedrilldownfilter"></a>

The time range drill down filter\.

## Syntax<a name="aws-properties-quicksight-template-timerangedrilldownfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-timerangedrilldownfilter-syntax.json"></a>

```
{
  "[Column](#cfn-quicksight-template-timerangedrilldownfilter-column)" : ColumnIdentifier,
  "[RangeMaximum](#cfn-quicksight-template-timerangedrilldownfilter-rangemaximum)" : String,
  "[RangeMinimum](#cfn-quicksight-template-timerangedrilldownfilter-rangeminimum)" : String,
  "[TimeGranularity](#cfn-quicksight-template-timerangedrilldownfilter-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-timerangedrilldownfilter-syntax.yaml"></a>

```
  [Column](#cfn-quicksight-template-timerangedrilldownfilter-column): 
    ColumnIdentifier
  [RangeMaximum](#cfn-quicksight-template-timerangedrilldownfilter-rangemaximum): String
  [RangeMinimum](#cfn-quicksight-template-timerangedrilldownfilter-rangeminimum): String
  [TimeGranularity](#cfn-quicksight-template-timerangedrilldownfilter-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-template-timerangedrilldownfilter-properties"></a>

`Column`  <a name="cfn-quicksight-template-timerangedrilldownfilter-column"></a>
The column that the filter is applied to\.  
*Required*: Yes  
*Type*: [ColumnIdentifier](aws-properties-quicksight-template-columnidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMaximum`  <a name="cfn-quicksight-template-timerangedrilldownfilter-rangemaximum"></a>
The maximum value for the filter value range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RangeMinimum`  <a name="cfn-quicksight-template-timerangedrilldownfilter-rangeminimum"></a>
The minimum value for the filter value range\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-template-timerangedrilldownfilter-timegranularity"></a>
The level of time precision that is used to aggregate `DateTime` values\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)