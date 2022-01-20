# AWS::ElastiCache::CacheCluster LogDeliveryConfigurationRequest<a name="aws-properties-elasticache-cachecluster-logdeliveryconfigurationrequest"></a>

Specifies the destination, format and type of the logs\. 

## Syntax<a name="aws-properties-elasticache-cachecluster-logdeliveryconfigurationrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-cachecluster-logdeliveryconfigurationrequest-syntax.json"></a>

```
{
  "[DestinationDetails](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-destinationdetails)" : DestinationDetails,
  "[DestinationType](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-destinationtype)" : String,
  "[LogFormat](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-logformat)" : String,
  "[LogType](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-logtype)" : String
}
```

### YAML<a name="aws-properties-elasticache-cachecluster-logdeliveryconfigurationrequest-syntax.yaml"></a>

```
  [DestinationDetails](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-destinationdetails): 
    DestinationDetails
  [DestinationType](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-destinationtype): String
  [LogFormat](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-logformat): String
  [LogType](#cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-logtype): String
```

## Properties<a name="aws-properties-elasticache-cachecluster-logdeliveryconfigurationrequest-properties"></a>

`DestinationDetails`  <a name="cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-destinationdetails"></a>
Configuration details of either a CloudWatch Logs destination or Kinesis Data Firehose destination\.  
*Required*: Yes  
*Type*: [DestinationDetails](aws-properties-elasticache-cachecluster-destinationdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationType`  <a name="cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-destinationtype"></a>
Specify either CloudWatch Logs or Kinesis Data Firehose as the destination type\. Valid values are either `cloudwatch-logs` or `kinesis-firehose`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogFormat`  <a name="cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-logformat"></a>
Valid values are either `json` or `text`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogType`  <a name="cfn-elasticache-cachecluster-logdeliveryconfigurationrequest-logtype"></a>
Valid value is either `slow-log`, which refers to [slow\-log](https://redis.io/commands/slowlog) or `engine-log`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)