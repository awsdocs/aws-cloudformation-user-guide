# AWS::QuickSight::Dashboard Computation<a name="aws-properties-quicksight-dashboard-computation"></a>

The computation union that is used in an insight visual\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-computation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-computation-syntax.json"></a>

```
{
  "[Forecast](#cfn-quicksight-dashboard-computation-forecast)" : ForecastComputation,
  "[GrowthRate](#cfn-quicksight-dashboard-computation-growthrate)" : GrowthRateComputation,
  "[MaximumMinimum](#cfn-quicksight-dashboard-computation-maximumminimum)" : MaximumMinimumComputation,
  "[MetricComparison](#cfn-quicksight-dashboard-computation-metriccomparison)" : MetricComparisonComputation,
  "[PeriodOverPeriod](#cfn-quicksight-dashboard-computation-periodoverperiod)" : PeriodOverPeriodComputation,
  "[PeriodToDate](#cfn-quicksight-dashboard-computation-periodtodate)" : PeriodToDateComputation,
  "[TopBottomMovers](#cfn-quicksight-dashboard-computation-topbottommovers)" : TopBottomMoversComputation,
  "[TopBottomRanked](#cfn-quicksight-dashboard-computation-topbottomranked)" : TopBottomRankedComputation,
  "[TotalAggregation](#cfn-quicksight-dashboard-computation-totalaggregation)" : TotalAggregationComputation,
  "[UniqueValues](#cfn-quicksight-dashboard-computation-uniquevalues)" : UniqueValuesComputation
}
```

### YAML<a name="aws-properties-quicksight-dashboard-computation-syntax.yaml"></a>

```
  [Forecast](#cfn-quicksight-dashboard-computation-forecast): 
    ForecastComputation
  [GrowthRate](#cfn-quicksight-dashboard-computation-growthrate): 
    GrowthRateComputation
  [MaximumMinimum](#cfn-quicksight-dashboard-computation-maximumminimum): 
    MaximumMinimumComputation
  [MetricComparison](#cfn-quicksight-dashboard-computation-metriccomparison): 
    MetricComparisonComputation
  [PeriodOverPeriod](#cfn-quicksight-dashboard-computation-periodoverperiod): 
    PeriodOverPeriodComputation
  [PeriodToDate](#cfn-quicksight-dashboard-computation-periodtodate): 
    PeriodToDateComputation
  [TopBottomMovers](#cfn-quicksight-dashboard-computation-topbottommovers): 
    TopBottomMoversComputation
  [TopBottomRanked](#cfn-quicksight-dashboard-computation-topbottomranked): 
    TopBottomRankedComputation
  [TotalAggregation](#cfn-quicksight-dashboard-computation-totalaggregation): 
    TotalAggregationComputation
  [UniqueValues](#cfn-quicksight-dashboard-computation-uniquevalues): 
    UniqueValuesComputation
```

## Properties<a name="aws-properties-quicksight-dashboard-computation-properties"></a>

`Forecast`  <a name="cfn-quicksight-dashboard-computation-forecast"></a>
The forecast computation configuration\.  
*Required*: No  
*Type*: [ForecastComputation](aws-properties-quicksight-dashboard-forecastcomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrowthRate`  <a name="cfn-quicksight-dashboard-computation-growthrate"></a>
The growth rate computation configuration\.  
*Required*: No  
*Type*: [GrowthRateComputation](aws-properties-quicksight-dashboard-growthratecomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumMinimum`  <a name="cfn-quicksight-dashboard-computation-maximumminimum"></a>
The maximum and minimum computation configuration\.  
*Required*: No  
*Type*: [MaximumMinimumComputation](aws-properties-quicksight-dashboard-maximumminimumcomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricComparison`  <a name="cfn-quicksight-dashboard-computation-metriccomparison"></a>
The metric comparison computation configuration\.  
*Required*: No  
*Type*: [MetricComparisonComputation](aws-properties-quicksight-dashboard-metriccomparisoncomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodOverPeriod`  <a name="cfn-quicksight-dashboard-computation-periodoverperiod"></a>
The period over period computation configuration\.  
*Required*: No  
*Type*: [PeriodOverPeriodComputation](aws-properties-quicksight-dashboard-periodoverperiodcomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodToDate`  <a name="cfn-quicksight-dashboard-computation-periodtodate"></a>
The period to `DataSetIdentifier` computation configuration\.  
*Required*: No  
*Type*: [PeriodToDateComputation](aws-properties-quicksight-dashboard-periodtodatecomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopBottomMovers`  <a name="cfn-quicksight-dashboard-computation-topbottommovers"></a>
The top movers and bottom movers computation configuration\.  
*Required*: No  
*Type*: [TopBottomMoversComputation](aws-properties-quicksight-dashboard-topbottommoverscomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopBottomRanked`  <a name="cfn-quicksight-dashboard-computation-topbottomranked"></a>
The top ranked and bottom ranked computation configuration\.  
*Required*: No  
*Type*: [TopBottomRankedComputation](aws-properties-quicksight-dashboard-topbottomrankedcomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalAggregation`  <a name="cfn-quicksight-dashboard-computation-totalaggregation"></a>
The total aggregation computation configuration\.  
*Required*: No  
*Type*: [TotalAggregationComputation](aws-properties-quicksight-dashboard-totalaggregationcomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UniqueValues`  <a name="cfn-quicksight-dashboard-computation-uniquevalues"></a>
The unique values computation configuration\.  
*Required*: No  
*Type*: [UniqueValuesComputation](aws-properties-quicksight-dashboard-uniquevaluescomputation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)