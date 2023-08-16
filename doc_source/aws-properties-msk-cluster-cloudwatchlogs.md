# AWS::MSK::Cluster CloudWatchLogs<a name="aws-properties-msk-cluster-cloudwatchlogs"></a>

Details of the CloudWatch Logs destination for broker logs\.

## Syntax<a name="aws-properties-msk-cluster-cloudwatchlogs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-cloudwatchlogs-syntax.json"></a>

```
{
  "[Enabled](#cfn-msk-cluster-cloudwatchlogs-enabled)" : Boolean,
  "[LogGroup](#cfn-msk-cluster-cloudwatchlogs-loggroup)" : String
}
```

### YAML<a name="aws-properties-msk-cluster-cloudwatchlogs-syntax.yaml"></a>

```
  [Enabled](#cfn-msk-cluster-cloudwatchlogs-enabled): Boolean
  [LogGroup](#cfn-msk-cluster-cloudwatchlogs-loggroup): String
```

## Properties<a name="aws-properties-msk-cluster-cloudwatchlogs-properties"></a>

`Enabled`  <a name="cfn-msk-cluster-cloudwatchlogs-enabled"></a>
Specifies whether broker logs get sent to the specified CloudWatch Logs destination\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogGroup`  <a name="cfn-msk-cluster-cloudwatchlogs-loggroup"></a>
The CloudWatch log group that is the destination for broker logs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)