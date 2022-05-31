# AWS::KinesisFirehose::DeliveryStream DynamicPartitioningConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration"></a>

The `DynamicPartitioningConfiguration` property type specifies the configuration of the dynamic partitioning mechanism that creates targeted data sets from the streaming data by partitioning it based on partition keys\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-syntax.json"></a>

```
{
  "[Enabled](#cfn-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-enabled)" : Boolean,
  "[RetryOptions](#cfn-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-retryoptions)" : RetryOptions
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-syntax.yaml"></a>

```
  [Enabled](#cfn-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-enabled): Boolean
  [RetryOptions](#cfn-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-retryoptions): 
    RetryOptions
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-properties"></a>

`Enabled`  <a name="cfn-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-enabled"></a>
Specifies whether dynamic partitioning is enabled for this Kinesis Data Firehose delivery stream\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryOptions`  <a name="cfn-kinesisfirehose-deliverystream-dynamicpartitioningconfiguration-retryoptions"></a>
Specifies the retry behavior in case Kinesis Data Firehose is unable to deliver data to an Amazon S3 prefix\.  
*Required*: No  
*Type*: [RetryOptions](aws-properties-kinesisfirehose-deliverystream-retryoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)