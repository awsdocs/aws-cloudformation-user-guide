# AWS::EC2::NetworkPerformanceMetricSubscription<a name="aws-resource-ec2-networkperformancemetricsubscription"></a>

Describes Infrastructure Performance subscriptions\.

## Syntax<a name="aws-resource-ec2-networkperformancemetricsubscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkperformancemetricsubscription-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkPerformanceMetricSubscription",
  "Properties" : {
      "[Destination](#cfn-ec2-networkperformancemetricsubscription-destination)" : String,
      "[Metric](#cfn-ec2-networkperformancemetricsubscription-metric)" : String,
      "[Source](#cfn-ec2-networkperformancemetricsubscription-source)" : String,
      "[Statistic](#cfn-ec2-networkperformancemetricsubscription-statistic)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-networkperformancemetricsubscription-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkPerformanceMetricSubscription
Properties: 
  [Destination](#cfn-ec2-networkperformancemetricsubscription-destination): String
  [Metric](#cfn-ec2-networkperformancemetricsubscription-metric): String
  [Source](#cfn-ec2-networkperformancemetricsubscription-source): String
  [Statistic](#cfn-ec2-networkperformancemetricsubscription-statistic): String
```

## Properties<a name="aws-resource-ec2-networkperformancemetricsubscription-properties"></a>

`Destination`  <a name="cfn-ec2-networkperformancemetricsubscription-destination"></a>
The Region or Availability Zone that's the target for the subscription\. For example, `eu-west-1`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Metric`  <a name="cfn-ec2-networkperformancemetricsubscription-metric"></a>
The metric used for the subscription\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `aggregate-latency`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Source`  <a name="cfn-ec2-networkperformancemetricsubscription-source"></a>
The Region or Availability Zone that's the source for the subscription\. For example, `us-east-1`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Statistic`  <a name="cfn-ec2-networkperformancemetricsubscription-statistic"></a>
The statistic used for the subscription\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `p50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-networkperformancemetricsubscription-return-values"></a>

### Ref<a name="aws-resource-ec2-networkperformancemetricsubscription-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `primaryIdentifier` property, which consists of the following properties: `source`, `destination`, `metric`, and `statistic`, with each value separated by a pipe \(\|\)\. For example, `{ "Ref": "us-east-1|us-east-2|aggregate-latency|p50" }`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.