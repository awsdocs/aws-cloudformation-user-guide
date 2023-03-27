# AWS::IoTSiteWise::AssetModel TumblingWindow<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow"></a>

Contains a tumbling window, which is a repeating fixed\-sized, non\-overlapping, and contiguous time window\. You can use this window in metrics to aggregate data from properties and other assets\.

You can use `m`, `h`, `d`, and `w` when you specify an interval or offset\. Note that `m` represents minutes, `h` represents hours, `d` represents days, and `w` represents weeks\. You can also use `s` to represent seconds in `offset`\.

The `interval` and `offset` parameters support the [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601)\. For example, `PT5S` represents 5 seconds, `PT5M` represents 5 minutes, and `PT5H` represents 5 hours\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-syntax.json"></a>

```
{
  "[Interval](#cfn-iotsitewise-assetmodel-tumblingwindow-interval)" : String,
  "[Offset](#cfn-iotsitewise-assetmodel-tumblingwindow-offset)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-syntax.yaml"></a>

```
  [Interval](#cfn-iotsitewise-assetmodel-tumblingwindow-interval): String
  [Offset](#cfn-iotsitewise-assetmodel-tumblingwindow-offset): String
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-properties"></a>

`Interval`  <a name="cfn-iotsitewise-assetmodel-tumblingwindow-interval"></a>
The time interval for the tumbling window\. The interval time must be between 1 minute and 1 week\.  
 AWS IoT SiteWise computes the `1w` interval the end of Sunday at midnight each week \(UTC\), the `1d` interval at the end of each day at midnight \(UTC\), the `1h` interval at the end of each hour, and so on\.   
When AWS IoT SiteWise aggregates data points for metric computations, the start of each interval is exclusive and the end of each interval is inclusive\. AWS IoT SiteWise places the computed data point at the end of the interval\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Offset`  <a name="cfn-iotsitewise-assetmodel-tumblingwindow-offset"></a>
The offset for the tumbling window\. The `offset` parameter accepts the following:  
+ The offset time\.

  For example, if you specify `18h` for `offset` and `1d` for `interval`, AWS IoT SiteWise aggregates data in one of the following ways:
  + If you create the metric before or at 6 PM \(UTC\), you get the first aggregation result at 6 PM \(UTC\) on the day when you create the metric\.
  + If you create the metric after 6 PM \(UTC\), you get the first aggregation result at 6 PM \(UTC\) the next day\.
+ The ISO 8601 format\.

  For example, if you specify `PT18H` for `offset` and `1d` for `interval`, AWS IoT SiteWise aggregates data in one of the following ways:
  + If you create the metric before or at 6 PM \(UTC\), you get the first aggregation result at 6 PM \(UTC\) on the day when you create the metric\.
  + If you create the metric after 6 PM \(UTC\), you get the first aggregation result at 6 PM \(UTC\) the next day\.
+ The 24\-hour clock\.

  For example, if you specify `00:03:00` for `offset`, `5m` for `interval`, and you create the metric at 2 PM \(UTC\), you get the first aggregation result at 2:03 PM \(UTC\)\. You get the second aggregation result at 2:08 PM \(UTC\)\. 
+ The offset time zone\.

  For example, if you specify `2021-07-23T18:00-08` for `offset` and `1d` for `interval`, AWS IoT SiteWise aggregates data in one of the following ways:
  + If you create the metric before or at 6 PM \(PST\), you get the first aggregation result at 6 PM \(PST\) on the day when you create the metric\.
  + If you create the metric after 6 PM \(PST\), you get the first aggregation result at 6 PM \(PST\) the next day\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)