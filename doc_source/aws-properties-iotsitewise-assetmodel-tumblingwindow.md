# AWS::IoTSiteWise::AssetModel TumblingWindow<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow"></a>

Contains a tumbling window, which is a repeating fixed\-sized, non\-overlapping, and contiguous time interval\. This window is used in metric and aggregation computations\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-syntax.json"></a>

```
{
  "[Interval](#cfn-iotsitewise-assetmodel-tumblingwindow-interval)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-syntax.yaml"></a>

```
  [Interval](#cfn-iotsitewise-assetmodel-tumblingwindow-interval): String
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-tumblingwindow-properties"></a>

`Interval`  <a name="cfn-iotsitewise-assetmodel-tumblingwindow-interval"></a>
The time interval for the tumbling window\. Note that `w` represents weeks, `d` represents days, `h` represents hours, and `m` represents minutes\. AWS IoT SiteWise computes the `1w` interval the end of Sunday at midnight each week \(UTC\), the `1d` interval at the end of each day at midnight \(UTC\), the `1h` interval at the end of each hour, and so on\.   
When AWS IoT SiteWise aggregates data points for metric computations, the start of each interval is exclusive and the end of each interval is inclusive\. AWS IoT SiteWise places the computed data point at the end of the interval\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)