# AWS::ElastiCache::CacheCluster CloudWatchLogsDestinationDetails<a name="aws-properties-elasticache-cachecluster-cloudwatchlogsdestinationdetails"></a>

Configuration details of a CloudWatch Logs destination\. Note that this field is marked as required but only if CloudWatch Logs was chosen as the destination\.

## Syntax<a name="aws-properties-elasticache-cachecluster-cloudwatchlogsdestinationdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-cachecluster-cloudwatchlogsdestinationdetails-syntax.json"></a>

```
{
  "[LogGroup](#cfn-elasticache-cachecluster-cloudwatchlogsdestinationdetails-loggroup)" : String
}
```

### YAML<a name="aws-properties-elasticache-cachecluster-cloudwatchlogsdestinationdetails-syntax.yaml"></a>

```
  [LogGroup](#cfn-elasticache-cachecluster-cloudwatchlogsdestinationdetails-loggroup): String
```

## Properties<a name="aws-properties-elasticache-cachecluster-cloudwatchlogsdestinationdetails-properties"></a>

`LogGroup`  <a name="cfn-elasticache-cachecluster-cloudwatchlogsdestinationdetails-loggroup"></a>
The name of the CloudWatch Logs log group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)