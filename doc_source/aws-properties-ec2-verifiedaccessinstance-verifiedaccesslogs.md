# AWS::EC2::VerifiedAccessInstance VerifiedAccessLogs<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesslogs"></a>

Describes the options for Verified Access logs\.

## Syntax<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesslogs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesslogs-syntax.json"></a>

```
{
  "[CloudWatchLogs](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-cloudwatchlogs)" : CloudWatchLogs,
  "[IncludeTrustContext](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-includetrustcontext)" : Boolean,
  "[KinesisDataFirehose](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-kinesisdatafirehose)" : KinesisDataFirehose,
  "[LogVersion](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-logversion)" : String,
  "[S3](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-s3)" : S3
}
```

### YAML<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesslogs-syntax.yaml"></a>

```
  [CloudWatchLogs](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-cloudwatchlogs): 
    CloudWatchLogs
  [IncludeTrustContext](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-includetrustcontext): Boolean
  [KinesisDataFirehose](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-kinesisdatafirehose): 
    KinesisDataFirehose
  [LogVersion](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-logversion): String
  [S3](#cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-s3): 
    S3
```

## Properties<a name="aws-properties-ec2-verifiedaccessinstance-verifiedaccesslogs-properties"></a>

`CloudWatchLogs`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-cloudwatchlogs"></a>
CloudWatch Logs logging destination\.  
*Required*: No  
*Type*: [CloudWatchLogs](aws-properties-ec2-verifiedaccessinstance-cloudwatchlogs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeTrustContext`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-includetrustcontext"></a>
 Include trust data sent by trust providers into the logs\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisDataFirehose`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-kinesisdatafirehose"></a>
Kinesis logging destination\.  
*Required*: No  
*Type*: [KinesisDataFirehose](aws-properties-ec2-verifiedaccessinstance-kinesisdatafirehose.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogVersion`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-logversion"></a>
 The logging version to use\.   
Valid values: `ocsf-0.1` \| `ocsf-1.0.0-rc.2`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesslogs-s3"></a>
Amazon S3 logging options\.  
*Required*: No  
*Type*: [S3](aws-properties-ec2-verifiedaccessinstance-s3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)