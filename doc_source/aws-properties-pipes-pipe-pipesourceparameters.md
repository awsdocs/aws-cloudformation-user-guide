# AWS::Pipes::Pipe PipeSourceParameters<a name="aws-properties-pipes-pipe-pipesourceparameters"></a>

The parameters required to set up a source for your pipe\.

## Syntax<a name="aws-properties-pipes-pipe-pipesourceparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipesourceparameters-syntax.json"></a>

```
{
  "[ActiveMQBrokerParameters](#cfn-pipes-pipe-pipesourceparameters-activemqbrokerparameters)" : PipeSourceActiveMQBrokerParameters,
  "[DynamoDBStreamParameters](#cfn-pipes-pipe-pipesourceparameters-dynamodbstreamparameters)" : PipeSourceDynamoDBStreamParameters,
  "[FilterCriteria](#cfn-pipes-pipe-pipesourceparameters-filtercriteria)" : FilterCriteria,
  "[KinesisStreamParameters](#cfn-pipes-pipe-pipesourceparameters-kinesisstreamparameters)" : PipeSourceKinesisStreamParameters,
  "[ManagedStreamingKafkaParameters](#cfn-pipes-pipe-pipesourceparameters-managedstreamingkafkaparameters)" : PipeSourceManagedStreamingKafkaParameters,
  "[RabbitMQBrokerParameters](#cfn-pipes-pipe-pipesourceparameters-rabbitmqbrokerparameters)" : PipeSourceRabbitMQBrokerParameters,
  "[SelfManagedKafkaParameters](#cfn-pipes-pipe-pipesourceparameters-selfmanagedkafkaparameters)" : PipeSourceSelfManagedKafkaParameters,
  "[SqsQueueParameters](#cfn-pipes-pipe-pipesourceparameters-sqsqueueparameters)" : PipeSourceSqsQueueParameters
}
```

### YAML<a name="aws-properties-pipes-pipe-pipesourceparameters-syntax.yaml"></a>

```
  [ActiveMQBrokerParameters](#cfn-pipes-pipe-pipesourceparameters-activemqbrokerparameters): 
    PipeSourceActiveMQBrokerParameters
  [DynamoDBStreamParameters](#cfn-pipes-pipe-pipesourceparameters-dynamodbstreamparameters): 
    PipeSourceDynamoDBStreamParameters
  [FilterCriteria](#cfn-pipes-pipe-pipesourceparameters-filtercriteria): 
    FilterCriteria
  [KinesisStreamParameters](#cfn-pipes-pipe-pipesourceparameters-kinesisstreamparameters): 
    PipeSourceKinesisStreamParameters
  [ManagedStreamingKafkaParameters](#cfn-pipes-pipe-pipesourceparameters-managedstreamingkafkaparameters): 
    PipeSourceManagedStreamingKafkaParameters
  [RabbitMQBrokerParameters](#cfn-pipes-pipe-pipesourceparameters-rabbitmqbrokerparameters): 
    PipeSourceRabbitMQBrokerParameters
  [SelfManagedKafkaParameters](#cfn-pipes-pipe-pipesourceparameters-selfmanagedkafkaparameters): 
    PipeSourceSelfManagedKafkaParameters
  [SqsQueueParameters](#cfn-pipes-pipe-pipesourceparameters-sqsqueueparameters): 
    PipeSourceSqsQueueParameters
```

## Properties<a name="aws-properties-pipes-pipe-pipesourceparameters-properties"></a>

`ActiveMQBrokerParameters`  <a name="cfn-pipes-pipe-pipesourceparameters-activemqbrokerparameters"></a>
The parameters for using an Active MQ broker as a source\.  
*Required*: No  
*Type*: [PipeSourceActiveMQBrokerParameters](aws-properties-pipes-pipe-pipesourceactivemqbrokerparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDBStreamParameters`  <a name="cfn-pipes-pipe-pipesourceparameters-dynamodbstreamparameters"></a>
The parameters for using a DynamoDB stream as a source\.  
*Required*: No  
*Type*: [PipeSourceDynamoDBStreamParameters](aws-properties-pipes-pipe-pipesourcedynamodbstreamparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FilterCriteria`  <a name="cfn-pipes-pipe-pipesourceparameters-filtercriteria"></a>
The collection of event patterns used to filter events\. For more information, see [Events and Event Patterns](https://docs.aws.amazon.com/eventbridge/latest/userguide/eventbridge-and-event-patterns.html) in the *Amazon EventBridge User Guide*\.  
*Required*: No  
*Type*: [FilterCriteria](aws-properties-pipes-pipe-filtercriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KinesisStreamParameters`  <a name="cfn-pipes-pipe-pipesourceparameters-kinesisstreamparameters"></a>
The parameters for using a Kinesis stream as a source\.  
*Required*: No  
*Type*: [PipeSourceKinesisStreamParameters](aws-properties-pipes-pipe-pipesourcekinesisstreamparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedStreamingKafkaParameters`  <a name="cfn-pipes-pipe-pipesourceparameters-managedstreamingkafkaparameters"></a>
The parameters for using an MSK stream as a source\.  
*Required*: No  
*Type*: [PipeSourceManagedStreamingKafkaParameters](aws-properties-pipes-pipe-pipesourcemanagedstreamingkafkaparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RabbitMQBrokerParameters`  <a name="cfn-pipes-pipe-pipesourceparameters-rabbitmqbrokerparameters"></a>
The parameters for using a Rabbit MQ broker as a source\.  
*Required*: No  
*Type*: [PipeSourceRabbitMQBrokerParameters](aws-properties-pipes-pipe-pipesourcerabbitmqbrokerparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelfManagedKafkaParameters`  <a name="cfn-pipes-pipe-pipesourceparameters-selfmanagedkafkaparameters"></a>
The parameters for using a self\-managed Apache Kafka stream as a source\.  
*Required*: No  
*Type*: [PipeSourceSelfManagedKafkaParameters](aws-properties-pipes-pipe-pipesourceselfmanagedkafkaparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqsQueueParameters`  <a name="cfn-pipes-pipe-pipesourceparameters-sqsqueueparameters"></a>
The parameters for using a Amazon SQS stream as a source\.  
*Required*: No  
*Type*: [PipeSourceSqsQueueParameters](aws-properties-pipes-pipe-pipesourcesqsqueueparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)