# AWS::ElastiCache::ReplicationGroup CloudWatchLogsDestinationDetails<a name="aws-properties-elasticache-replicationgroup-cloudwatchlogsdestinationdetails"></a>

The configuration details of the CloudWatch Logs destination\. Note that this field is marked as required but only if CloudWatch Logs was chosen as the destination\.

## Syntax<a name="aws-properties-elasticache-replicationgroup-cloudwatchlogsdestinationdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-replicationgroup-cloudwatchlogsdestinationdetails-syntax.json"></a>

```
{
  "[LogGroup](#cfn-elasticache-replicationgroup-cloudwatchlogsdestinationdetails-loggroup)" : String
}
```

### YAML<a name="aws-properties-elasticache-replicationgroup-cloudwatchlogsdestinationdetails-syntax.yaml"></a>

```
  [LogGroup](#cfn-elasticache-replicationgroup-cloudwatchlogsdestinationdetails-loggroup): String
```

## Properties<a name="aws-properties-elasticache-replicationgroup-cloudwatchlogsdestinationdetails-properties"></a>

`LogGroup`  <a name="cfn-elasticache-replicationgroup-cloudwatchlogsdestinationdetails-loggroup"></a>
The name of the CloudWatch Logs log group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)