# AWS::IoTSiteWise::AssetModel Metric<a name="aws-properties-iotsitewise-assetmodel-metric"></a>

Contains an asset metric property\. With metrics, you can calculate aggregate functions, such as an average, maximum, or minimum, as specified through an expression\. A metric maps several values to a single value \(such as a sum\)\.

The maximum number of dependent/cascading variables used in any one metric calculation is 10\. Therefore, a *root* metric can have up to 10 cascading metrics in its computational dependency tree\. Additionally, a metric can only have a data type of `DOUBLE` and consume properties with data types of `INTEGER` or `DOUBLE`\.

For more information, see [Defining data properties](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/asset-properties.html#metrics) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-metric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-metric-syntax.json"></a>

```
{
  "[Expression](#cfn-iotsitewise-assetmodel-metric-expression)" : String,
  "[Variables](#cfn-iotsitewise-assetmodel-metric-variables)" : [ ExpressionVariable, ... ],
  "[Window](#cfn-iotsitewise-assetmodel-metric-window)" : MetricWindow
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-metric-syntax.yaml"></a>

```
  [Expression](#cfn-iotsitewise-assetmodel-metric-expression): String
  [Variables](#cfn-iotsitewise-assetmodel-metric-variables): 
    - ExpressionVariable
  [Window](#cfn-iotsitewise-assetmodel-metric-window): 
    MetricWindow
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-metric-properties"></a>

`Expression`  <a name="cfn-iotsitewise-assetmodel-metric-expression"></a>
The mathematical expression that defines the metric aggregation function\. You can specify up to 10 variables per expression\. You can specify up to 10 functions per expression\.   
For more information, see [Quotas](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/quotas.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variables`  <a name="cfn-iotsitewise-assetmodel-metric-variables"></a>
The list of variables used in the expression\.  
*Required*: Yes  
*Type*: List of [ExpressionVariable](aws-properties-iotsitewise-assetmodel-expressionvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Window`  <a name="cfn-iotsitewise-assetmodel-metric-window"></a>
The window \(time interval\) over which AWS IoT SiteWise computes the metric's aggregation expression\. AWS IoT SiteWise computes one data point per `window`\.  
*Required*: Yes  
*Type*: [MetricWindow](aws-properties-iotsitewise-assetmodel-metricwindow.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)