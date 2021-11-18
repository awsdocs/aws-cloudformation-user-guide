# AWS::ElastiCache::CacheCluster KinesisFirehoseDestinationDetails<a name="aws-properties-elasticache-cachecluster-kinesisfirehosedestinationdetails"></a>

The configuration details of the Kinesis Data Firehose destination\. Note that this field is marked as required but only if Kinesis Data Firehose was chosen as the destination\.

## Syntax<a name="aws-properties-elasticache-cachecluster-kinesisfirehosedestinationdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-cachecluster-kinesisfirehosedestinationdetails-syntax.json"></a>

```
{
  "[DeliveryStream](#cfn-elasticache-cachecluster-kinesisfirehosedestinationdetails-deliverystream)" : String
}
```

### YAML<a name="aws-properties-elasticache-cachecluster-kinesisfirehosedestinationdetails-syntax.yaml"></a>

```
  [DeliveryStream](#cfn-elasticache-cachecluster-kinesisfirehosedestinationdetails-deliverystream): String
```

## Properties<a name="aws-properties-elasticache-cachecluster-kinesisfirehosedestinationdetails-properties"></a>

`DeliveryStream`  <a name="cfn-elasticache-cachecluster-kinesisfirehosedestinationdetails-deliverystream"></a>
The name of the Kinesis Data Firehose delivery stream\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)