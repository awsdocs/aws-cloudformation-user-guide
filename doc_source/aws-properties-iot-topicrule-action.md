# AWS IoT TopicRule Action<a name="aws-properties-iot-topicrule-action"></a>

`Action` is a property of the `TopicRulePayload` property that describes an action associated with an AWS IoT rule\. For more information, see [Rules for AWS IoT](http://docs.aws.amazon.com/iot/latest/developerguide/iot-rules.html)\.

## Syntax<a name="w3ab2c21c14e1317b5"></a>

### JSON<a name="aws-properties-iot-topicrule-action-syntax.json"></a>

```
{
  "[CloudwatchAlarm](#cfn-iot-topicrule-action-cloudwatchalarm)": CloudwatchAlarm Action,
  "[CloudwatchMetric](#cfn-iot-topicrule-action-cloudwatchmetric)": CloudwatchMetric Action,
  "[DynamoDB](#cfn-iot-topicrule-action-dynamodb)": DynamoDB Action,
  "[DynamoDBv2](#cfn-iot-topicrule-action-dynamodbv2)": DynamoDBv2 Action,
  "[Elasticsearch](#cfn-iot-topicrule-action-elasticsearch)": Elasticsearch Action,
  "[Firehose](#cfn-iot-topicrule-action-firehose)": Firehose Action,
  "[Kinesis](#cfn-iot-topicrule-action-kinesis)": Kinesis Action,
  "[Lambda](#cfn-iot-topicrule-action-lambda)": Lambda Action,
  "[Republish](#cfn-iot-topicrule-action-republish)": Republish Action,
  "[S3](#cfn-iot-topicrule-action-s3)": S3 Action,
  "[Sns](#cfn-iot-topicrule-action-sns)": Sns Action,
  "[Sqs](#cfn-iot-topicrule-action-sqs)": Sqs Action
}
```

### YAML<a name="aws-properties-iot-topicrule-action-syntax.yaml"></a>

```
[CloudwatchAlarm](#cfn-iot-topicrule-action-cloudwatchalarm):
  CloudwatchAlarm Action
[CloudwatchMetric](#cfn-iot-topicrule-action-cloudwatchmetric):
  CloudwatchMetric Action
[DynamoDB](#cfn-iot-topicrule-action-dynamodb):
  DynamoDB Action
[DynamoDBv2](#cfn-iot-topicrule-action-dynamodbv2):
  DynamoDBv2 Action
[Elasticsearch](#cfn-iot-topicrule-action-elasticsearch):
  Elasticsearch Action
[Firehose](#cfn-iot-topicrule-action-firehose):
  Firehose Action
[Kinesis](#cfn-iot-topicrule-action-kinesis):
  Kinesis Action
[Lambda](#cfn-iot-topicrule-action-lambda):
  Lambda Action
[Republish](#cfn-iot-topicrule-action-republish):
  Republish Action
[S3](#cfn-iot-topicrule-action-s3):
  S3 Action
[Sns](#cfn-iot-topicrule-action-sns):
  Sns Action
[Sqs](#cfn-iot-topicrule-action-sqs):
  Sqs Action
```

## Properties<a name="w3ab2c21c14e1317b7"></a>

`CloudwatchAlarm`  <a name="cfn-iot-topicrule-action-cloudwatchalarm"></a>
Changes the state of a CloudWatch alarm\.  
*Required*: No  
*Type*: [AWS IoT TopicRule CloudwatchAlarmAction](aws-properties-iot-topicrule-cloudwatchalarmaction.md)

`CloudwatchMetric`  <a name="cfn-iot-topicrule-action-cloudwatchmetric"></a>
Captures a CloudWatch metric\.  
*Required*: No  
*Type*: [AWS IoT TopicRule CloudwatchMetricAction](aws-properties-iot-topicrule-cloudwatchmetricaction.md)

`DynamoDB`  <a name="cfn-iot-topicrule-action-dynamodb"></a>
Writes data to a DynamoDB table\.  
*Required*: No  
*Type*: [AWS IoT TopicRule DynamoDBAction](aws-properties-iot-topicrule-dynamodbaction.md)

`DynamoDBv2`  <a name="cfn-iot-topicrule-action-dynamodbv2"></a>
Writes data to a DynamoDB table\.  
*Required*: No  
*Type*: [AWS IoT TopicRule DynamoDBv2Action](aws-properties-iot-topicrule-dynamodbv2action.md)

`Elasticsearch`  <a name="cfn-iot-topicrule-action-elasticsearch"></a>
Writes data to an Elasticsearch domain\.  
*Required*: No  
*Type*: [AWS IoT TopicRule ElasticsearchAction](aws-properties-iot-topicrule-elasticsearchaction.md)

`Firehose`  <a name="cfn-iot-topicrule-action-firehose"></a>
Writes data to a Kinesis Data Firehose stream\.  
*Required*: No  
*Type*: [AWS IoT TopicRule FirehoseAction](aws-properties-iot-topicrule-firehoseaction.md)

`Kinesis`  <a name="cfn-iot-topicrule-action-kinesis"></a>
Writes data to an Kinesis stream\.  
*Required*: No  
*Type*: [AWS IoT TopicRule KinesisAction](aws-properties-iot-topicrule-kinesisaction.md)

`Lambda`  <a name="cfn-iot-topicrule-action-lambda"></a>
Invokes a Lambda function\.  
*Required*: No  
*Type*: [AWS IoT TopicRule LambdaAction](aws-properties-iot-topicrule-lambdaaction.md)

`Republish`  <a name="cfn-iot-topicrule-action-republish"></a>
Publishes data to an MQ Telemetry Transport \(MQTT\) topic different from the one currently specified\.  
*Required*: No  
*Type*: [AWS IoT TopicRule RepublishAction](aws-properties-iot-topicrule-republishaction.md)

`S3`  <a name="cfn-iot-topicrule-action-s3"></a>
Writes data to an S3 bucket\.  
*Required*: No  
*Type*: [AWS IoT TopicRule S3Action](aws-properties-iot-topicrule-s3action.md)

`Sns`  <a name="cfn-iot-topicrule-action-sns"></a>
Publishes data to an SNS topic\.  
*Required*: No  
*Type*: [AWS IoT TopicRule SnsAction](aws-properties-iot-topicrule-snsaction.md)

`Sqs`  <a name="cfn-iot-topicrule-action-sqs"></a>
Publishes data to an SQS queue\.  
*Required*: No  
*Type*: [AWS IoT TopicRule SqsAction](aws-properties-iot-topicrule-sqsaction.md)