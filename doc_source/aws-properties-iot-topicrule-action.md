# AWS::IoT::TopicRule Action<a name="aws-properties-iot-topicrule-action"></a>

Describes the actions associated with a rule\.

## Syntax<a name="aws-properties-iot-topicrule-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-action-syntax.json"></a>

```
{
  "[CloudwatchAlarm](#cfn-iot-topicrule-action-cloudwatchalarm)" : CloudwatchAlarmAction,
  "[CloudwatchMetric](#cfn-iot-topicrule-action-cloudwatchmetric)" : CloudwatchMetricAction,
  "[DynamoDB](#cfn-iot-topicrule-action-dynamodb)" : DynamoDBAction,
  "[DynamoDBv2](#cfn-iot-topicrule-action-dynamodbv2)" : DynamoDBv2Action,
  "[Elasticsearch](#cfn-iot-topicrule-action-elasticsearch)" : ElasticsearchAction,
  "[Firehose](#cfn-iot-topicrule-action-firehose)" : FirehoseAction,
  "[Http](#cfn-iot-topicrule-action-http)" : HttpAction,
  "[IotAnalytics](#cfn-iot-topicrule-action-iotanalytics)" : IotAnalyticsAction,
  "[IotEvents](#cfn-iot-topicrule-action-iotevents)" : IotEventsAction,
  "[IotSiteWise](#cfn-iot-topicrule-action-iotsitewise)" : IotSiteWiseAction,
  "[Kinesis](#cfn-iot-topicrule-action-kinesis)" : KinesisAction,
  "[Lambda](#cfn-iot-topicrule-action-lambda)" : LambdaAction,
  "[Republish](#cfn-iot-topicrule-action-republish)" : RepublishAction,
  "[S3](#cfn-iot-topicrule-action-s3)" : S3Action,
  "[Sns](#cfn-iot-topicrule-action-sns)" : SnsAction,
  "[Sqs](#cfn-iot-topicrule-action-sqs)" : SqsAction,
  "[StepFunctions](#cfn-iot-topicrule-action-stepfunctions)" : StepFunctionsAction
}
```

### YAML<a name="aws-properties-iot-topicrule-action-syntax.yaml"></a>

```
  [CloudwatchAlarm](#cfn-iot-topicrule-action-cloudwatchalarm): 
    CloudwatchAlarmAction
  [CloudwatchMetric](#cfn-iot-topicrule-action-cloudwatchmetric): 
    CloudwatchMetricAction
  [DynamoDB](#cfn-iot-topicrule-action-dynamodb): 
    DynamoDBAction
  [DynamoDBv2](#cfn-iot-topicrule-action-dynamodbv2): 
    DynamoDBv2Action
  [Elasticsearch](#cfn-iot-topicrule-action-elasticsearch): 
    ElasticsearchAction
  [Firehose](#cfn-iot-topicrule-action-firehose): 
    FirehoseAction
  [Http](#cfn-iot-topicrule-action-http): 
    HttpAction
  [IotAnalytics](#cfn-iot-topicrule-action-iotanalytics): 
    IotAnalyticsAction
  [IotEvents](#cfn-iot-topicrule-action-iotevents): 
    IotEventsAction
  [IotSiteWise](#cfn-iot-topicrule-action-iotsitewise): 
    IotSiteWiseAction
  [Kinesis](#cfn-iot-topicrule-action-kinesis): 
    KinesisAction
  [Lambda](#cfn-iot-topicrule-action-lambda): 
    LambdaAction
  [Republish](#cfn-iot-topicrule-action-republish): 
    RepublishAction
  [S3](#cfn-iot-topicrule-action-s3): 
    S3Action
  [Sns](#cfn-iot-topicrule-action-sns): 
    SnsAction
  [Sqs](#cfn-iot-topicrule-action-sqs): 
    SqsAction
  [StepFunctions](#cfn-iot-topicrule-action-stepfunctions): 
    StepFunctionsAction
```

## Properties<a name="aws-properties-iot-topicrule-action-properties"></a>

`CloudwatchAlarm`  <a name="cfn-iot-topicrule-action-cloudwatchalarm"></a>
Change the state of a CloudWatch alarm\.  
*Required*: No  
*Type*: [CloudwatchAlarmAction](aws-properties-iot-topicrule-cloudwatchalarmaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudwatchMetric`  <a name="cfn-iot-topicrule-action-cloudwatchmetric"></a>
Capture a CloudWatch metric\.  
*Required*: No  
*Type*: [CloudwatchMetricAction](aws-properties-iot-topicrule-cloudwatchmetricaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDB`  <a name="cfn-iot-topicrule-action-dynamodb"></a>
Write to a DynamoDB table\.  
*Required*: No  
*Type*: [DynamoDBAction](aws-properties-iot-topicrule-dynamodbaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDBv2`  <a name="cfn-iot-topicrule-action-dynamodbv2"></a>
Write to a DynamoDB table\. This is a new version of the DynamoDB action\. It allows you to write each attribute in an MQTT message payload into a separate DynamoDB column\.  
*Required*: No  
*Type*: [DynamoDBv2Action](aws-properties-iot-topicrule-dynamodbv2action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Elasticsearch`  <a name="cfn-iot-topicrule-action-elasticsearch"></a>
Write data to an Amazon Elasticsearch Service domain\.  
*Required*: No  
*Type*: [ElasticsearchAction](aws-properties-iot-topicrule-elasticsearchaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Firehose`  <a name="cfn-iot-topicrule-action-firehose"></a>
Write to an Amazon Kinesis Firehose stream\.  
*Required*: No  
*Type*: [FirehoseAction](aws-properties-iot-topicrule-firehoseaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Http`  <a name="cfn-iot-topicrule-action-http"></a>
Send data to an HTTPS endpoint\.  
*Required*: No  
*Type*: [HttpAction](aws-properties-iot-topicrule-httpaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotAnalytics`  <a name="cfn-iot-topicrule-action-iotanalytics"></a>
Sends message data to an AWS IoT Analytics channel\.  
*Required*: No  
*Type*: [IotAnalyticsAction](aws-properties-iot-topicrule-iotanalyticsaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotEvents`  <a name="cfn-iot-topicrule-action-iotevents"></a>
Sends an input to an AWS IoT Events detector\.  
*Required*: No  
*Type*: [IotEventsAction](aws-properties-iot-topicrule-ioteventsaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IotSiteWise`  <a name="cfn-iot-topicrule-action-iotsitewise"></a>
Sends data from the MQTT message that triggered the rule to AWS IoT SiteWise asset properties\.  
*Required*: No  
*Type*: [IotSiteWiseAction](aws-properties-iot-topicrule-iotsitewiseaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Kinesis`  <a name="cfn-iot-topicrule-action-kinesis"></a>
Write data to an Amazon Kinesis stream\.  
*Required*: No  
*Type*: [KinesisAction](aws-properties-iot-topicrule-kinesisaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lambda`  <a name="cfn-iot-topicrule-action-lambda"></a>
Invoke a Lambda function\.  
*Required*: No  
*Type*: [LambdaAction](aws-properties-iot-topicrule-lambdaaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Republish`  <a name="cfn-iot-topicrule-action-republish"></a>
Publish to another MQTT topic\.  
*Required*: No  
*Type*: [RepublishAction](aws-properties-iot-topicrule-republishaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-iot-topicrule-action-s3"></a>
Write to an Amazon S3 bucket\.  
*Required*: No  
*Type*: [S3Action](aws-properties-iot-topicrule-s3action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sns`  <a name="cfn-iot-topicrule-action-sns"></a>
Publish to an Amazon SNS topic\.  
*Required*: No  
*Type*: [SnsAction](aws-properties-iot-topicrule-snsaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sqs`  <a name="cfn-iot-topicrule-action-sqs"></a>
Publish to an Amazon SQS queue\.  
*Required*: No  
*Type*: [SqsAction](aws-properties-iot-topicrule-sqsaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepFunctions`  <a name="cfn-iot-topicrule-action-stepfunctions"></a>
Starts execution of a Step Functions state machine\.  
*Required*: No  
*Type*: [StepFunctionsAction](aws-properties-iot-topicrule-stepfunctionsaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)