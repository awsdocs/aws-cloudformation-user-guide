# AWS::RUM::AppMonitor MetricDestination<a name="aws-properties-rum-appmonitor-metricdestination"></a>

Creates or updates a destination to receive extended metrics from CloudWatch RUM\. You can send extended metrics to CloudWatch or to a CloudWatch Evidently experiment\.

For more information about extended metrics, see [ Extended metrics that you can send to CloudWatch and CloudWatch Evidently](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-vended-metrics.html)\.

## Syntax<a name="aws-properties-rum-appmonitor-metricdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rum-appmonitor-metricdestination-syntax.json"></a>

```
{
  "[Destination](#cfn-rum-appmonitor-metricdestination-destination)" : String,
  "[DestinationArn](#cfn-rum-appmonitor-metricdestination-destinationarn)" : String,
  "[IamRoleArn](#cfn-rum-appmonitor-metricdestination-iamrolearn)" : String,
  "[MetricDefinitions](#cfn-rum-appmonitor-metricdestination-metricdefinitions)" : [ MetricDefinition, ... ]
}
```

### YAML<a name="aws-properties-rum-appmonitor-metricdestination-syntax.yaml"></a>

```
  [Destination](#cfn-rum-appmonitor-metricdestination-destination): String
  [DestinationArn](#cfn-rum-appmonitor-metricdestination-destinationarn): String
  [IamRoleArn](#cfn-rum-appmonitor-metricdestination-iamrolearn): String
  [MetricDefinitions](#cfn-rum-appmonitor-metricdestination-metricdefinitions): 
    - MetricDefinition
```

## Properties<a name="aws-properties-rum-appmonitor-metricdestination-properties"></a>

`Destination`  <a name="cfn-rum-appmonitor-metricdestination-destination"></a>
Defines the destination to send the metrics to\. Valid values are `CloudWatch` and `Evidently`\. If you specify `Evidently`, you must also specify the ARN of the CloudWatchEvidently experiment that is to be the destination and an IAM role that has permission to write to the experiment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationArn`  <a name="cfn-rum-appmonitor-metricdestination-destinationarn"></a>
Use this parameter only if `Destination` is `Evidently`\. This parameter specifies the ARN of the Evidently experiment that will receive the extended metrics\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRoleArn`  <a name="cfn-rum-appmonitor-metricdestination-iamrolearn"></a>
This parameter is required if `Destination` is `Evidently`\. If `Destination` is `CloudWatch`, do not use this parameter\.  
This parameter specifies the ARN of an IAM role that RUM will assume to write to the Evidently experiment that you are sending metrics to\. This role must have permission to write to that experiment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricDefinitions`  <a name="cfn-rum-appmonitor-metricdestination-metricdefinitions"></a>
An array of structures which define the metrics that you want to send\.  
*Required*: No  
*Type*: List of [MetricDefinition](aws-properties-rum-appmonitor-metricdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)