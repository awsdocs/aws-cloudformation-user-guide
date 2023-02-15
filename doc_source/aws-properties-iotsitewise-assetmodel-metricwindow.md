# AWS::IoTSiteWise::AssetModel MetricWindow<a name="aws-properties-iotsitewise-assetmodel-metricwindow"></a>

Contains a time interval window used for data aggregate computations \(for example, average, sum, count, and so on\)\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-metricwindow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-metricwindow-syntax.json"></a>

```
{
  "[Tumbling](#cfn-iotsitewise-assetmodel-metricwindow-tumbling)" : TumblingWindow
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-metricwindow-syntax.yaml"></a>

```
  [Tumbling](#cfn-iotsitewise-assetmodel-metricwindow-tumbling): 
    TumblingWindow
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-metricwindow-properties"></a>

`Tumbling`  <a name="cfn-iotsitewise-assetmodel-metricwindow-tumbling"></a>
The tumbling time interval window\.  
*Required*: No  
*Type*: [TumblingWindow](aws-properties-iotsitewise-assetmodel-tumblingwindow.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)