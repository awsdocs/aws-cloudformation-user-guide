# AWS::RUM::AppMonitor MetricDefinition<a name="aws-properties-rum-appmonitor-metricdefinition"></a>

Specifies the extended metrics that you want the CloudWatch RUM app monitor to send to a destination\. Valid destinations include CloudWatch and Evidently\.

By default, RUM app monitors send some metrics to CloudWatch\. These default metrics are listed in [CloudWatch metrics that you can collect with CloudWatch RUM](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-metrics.html)\.

If you also send extended metrics, you can send metrics to Evidently as well as CloudWatch, and you can also optionally send the metrics with additional dimensions\. The valid dimension names for the additional dimensions are `BrowserName`, `CountryCode`, `DeviceType`, `FileType`, `OSName`, and `PageId`\. For more information, see [ Extended metrics that you can send to CloudWatch and CloudWatch Evidently](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-vended-metrics.html)\.

The maximum number of metric definitions that one destination can contain is 2000\.

Extended metrics sent are charged as CloudWatch custom metrics\. Each combination of additional dimension name and dimension value counts as a custom metric\. 

If some metric definitions that you specify are not valid, then the operation will not modify any metric definitions even if other metric definitions specified are valid\.

## Syntax<a name="aws-properties-rum-appmonitor-metricdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rum-appmonitor-metricdefinition-syntax.json"></a>

```
{
  "[DimensionKeys](#cfn-rum-appmonitor-metricdefinition-dimensionkeys)" : {Key : Value, ...},
  "[EventPattern](#cfn-rum-appmonitor-metricdefinition-eventpattern)" : String,
  "[Name](#cfn-rum-appmonitor-metricdefinition-name)" : String,
  "[UnitLabel](#cfn-rum-appmonitor-metricdefinition-unitlabel)" : String,
  "[ValueKey](#cfn-rum-appmonitor-metricdefinition-valuekey)" : String
}
```

### YAML<a name="aws-properties-rum-appmonitor-metricdefinition-syntax.yaml"></a>

```
  [DimensionKeys](#cfn-rum-appmonitor-metricdefinition-dimensionkeys): 
    Key : Value
  [EventPattern](#cfn-rum-appmonitor-metricdefinition-eventpattern): String
  [Name](#cfn-rum-appmonitor-metricdefinition-name): String
  [UnitLabel](#cfn-rum-appmonitor-metricdefinition-unitlabel): String
  [ValueKey](#cfn-rum-appmonitor-metricdefinition-valuekey): String
```

## Properties<a name="aws-properties-rum-appmonitor-metricdefinition-properties"></a>

`DimensionKeys`  <a name="cfn-rum-appmonitor-metricdefinition-dimensionkeys"></a>
This field is a map of field paths to dimension names\. It defines the dimensions to associate with this metric in CloudWatch The value of this field is used only if the metric destination is `CloudWatch`\. If the metric destination is `Evidently`, the value of `DimensionKeys` is ignored\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventPattern`  <a name="cfn-rum-appmonitor-metricdefinition-eventpattern"></a>
The pattern that defines the metric\. RUM checks events that happen in a user's session against the pattern, and events that match the pattern are sent to the metric destination\.  
If the metrics destination is `CloudWatch` and the event also matches a value in `DimensionKeys`, then the metric is published with the specified dimensions\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-rum-appmonitor-metricdefinition-name"></a>
The name of the metric that is defined in this structure\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnitLabel`  <a name="cfn-rum-appmonitor-metricdefinition-unitlabel"></a>
Use this field only if you are sending this metric to CloudWatch\. It defines the CloudWatch metric unit that this metric is measured in\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueKey`  <a name="cfn-rum-appmonitor-metricdefinition-valuekey"></a>
The field within the event object that the metric value is sourced from\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)