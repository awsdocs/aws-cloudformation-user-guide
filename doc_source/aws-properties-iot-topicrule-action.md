# AWS IoT TopicRule Action<a name="aws-properties-iot-topicrule-action"></a>

`Action` is a property of the `TopicRulePayload` property that describes an action associated with an AWS IoT rule\. For more information, see [Rules for AWS IoT](http://docs.aws.amazon.com/iot/latest/developerguide/iot-rules.html)\.

## Syntax<a name="w3ab2c21c14e1120b5"></a>

### JSON<a name="aws-properties-iot-topicrule-action-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-cloudwatchalarm)": CloudwatchAlarm Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-cloudwatchmetric)": CloudwatchMetric Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-dynamodb)": DynamoDB Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-dynamodbv2)": DynamoDBv2 Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-elasticsearch)": Elasticsearch Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-firehose)": Firehose Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-kinesis)": Kinesis Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-lambda)": Lambda Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-republish)": Republish Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-s3)": S3 Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-sns)": Sns Action,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-sqs)": Sqs Action
}
```

### YAML<a name="aws-properties-iot-topicrule-action-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-cloudwatchalarm):
  CloudwatchAlarm Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-cloudwatchmetric):
  CloudwatchMetric Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-dynamodb):
  DynamoDB Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-dynamodbv2):
  DynamoDBv2 Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-elasticsearch):
  Elasticsearch Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-firehose):
  Firehose Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-kinesis):
  Kinesis Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-lambda):
  Lambda Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-republish):
  Republish Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-s3):
  S3 Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-sns):
  Sns Action
[[ERROR] BAD/MISSING LINK TEXT](#cfn-iot-topicrule-action-sqs):
  Sqs Action
```

## Properties<a name="w3ab2c21c14e1120b7"></a>

`CloudwatchAlarm`  
Changes the state of a CloudWatch alarm\.  
*Required: *No  
*Type*: 

`CloudwatchMetric`  
Captures a CloudWatch metric\.  
*Required: *No  
*Type*: 

`DynamoDB`  
Writes data to a DynamoDB table\.  
*Required: *No  
*Type*: 

`DynamoDBv2`  
Writes data to a DynamoDB table\.  
*Required: *No  
*Type*: 

`Elasticsearch`  
Writes data to an Elasticsearch domain\.  
*Required: *No  
*Type*: 

`Firehose`  
Writes data to a Kinesis Data Firehose stream\.  
*Required: *No  
*Type*: 

`Kinesis`  
Writes data to an Kinesis stream\.  
*Required: *No  
*Type*: 

`Lambda`  
Invokes a Lambda function\.  
*Required: *No  
*Type*: 

`Republish`  
Publishes data to an MQ Telemetry Transport \(MQTT\) topic different from the one currently specified\.  
*Required: *No  
*Type*: 

`S3`  
Writes data to an S3 bucket\.  
*Required: *No  
*Type*: 

`Sns`  
Publishes data to an SNS topic\.  
*Required: *No  
*Type*: 

`Sqs`  
Publishes data to an SQS queue\.  
*Required: *No  
*Type*: 