# AWS::MSK::Cluster BrokerLogs<a name="aws-properties-msk-cluster-brokerlogs"></a>

You can configure your MSK cluster to send broker logs to different destination types\. This configuration specifies the details of these destinations\.

## Syntax<a name="aws-properties-msk-cluster-brokerlogs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-brokerlogs-syntax.json"></a>

```
{
  "[CloudWatchLogs](#cfn-msk-cluster-brokerlogs-cloudwatchlogs)" : CloudWatchLogs,
  "[Firehose](#cfn-msk-cluster-brokerlogs-firehose)" : Firehose,
  "[S3](#cfn-msk-cluster-brokerlogs-s3)" : S3
}
```

### YAML<a name="aws-properties-msk-cluster-brokerlogs-syntax.yaml"></a>

```
  [CloudWatchLogs](#cfn-msk-cluster-brokerlogs-cloudwatchlogs): 
    CloudWatchLogs
  [Firehose](#cfn-msk-cluster-brokerlogs-firehose): 
    Firehose
  [S3](#cfn-msk-cluster-brokerlogs-s3): 
    S3
```

## Properties<a name="aws-properties-msk-cluster-brokerlogs-properties"></a>

`CloudWatchLogs`  <a name="cfn-msk-cluster-brokerlogs-cloudwatchlogs"></a>
Details of the CloudWatch Logs destination for broker logs\.  
*Required*: No  
*Type*: [CloudWatchLogs](aws-properties-msk-cluster-cloudwatchlogs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Firehose`  <a name="cfn-msk-cluster-brokerlogs-firehose"></a>
Details of the Kinesis Data Firehose delivery stream that is the destination for broker logs\.  
*Required*: No  
*Type*: [Firehose](aws-properties-msk-cluster-firehose.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-msk-cluster-brokerlogs-s3"></a>
Details of the Amazon S3 destination for broker logs\.  
*Required*: No  
*Type*: [S3](aws-properties-msk-cluster-s3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)