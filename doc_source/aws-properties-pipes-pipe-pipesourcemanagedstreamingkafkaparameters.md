# AWS::Pipes::Pipe PipeSourceManagedStreamingKafkaParameters<a name="aws-properties-pipes-pipe-pipesourcemanagedstreamingkafkaparameters"></a>

The parameters for using an MSK stream as a source\.

## Syntax<a name="aws-properties-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-syntax.json"></a>

```
{
  "[BatchSize](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-batchsize)" : Integer,
  "[ConsumerGroupID](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-consumergroupid)" : String,
  "[Credentials](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-credentials)" : MSKAccessCredentials,
  "[MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-maximumbatchingwindowinseconds)" : Integer,
  "[StartingPosition](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-startingposition)" : String,
  "[TopicName](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-topicname)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-syntax.yaml"></a>

```
  [BatchSize](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-batchsize): Integer
  [ConsumerGroupID](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-consumergroupid): String
  [Credentials](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-credentials): 
    MSKAccessCredentials
  [MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-maximumbatchingwindowinseconds): Integer
  [StartingPosition](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-startingposition): String
  [TopicName](#cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-topicname): String
```

## Properties<a name="aws-properties-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-properties"></a>

`BatchSize`  <a name="cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-batchsize"></a>
The maximum number of records to include in each batch\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConsumerGroupID`  <a name="cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-consumergroupid"></a>
The name of the destination queue to consume\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Credentials`  <a name="cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-credentials"></a>
The credentials needed to access the resource\.  
*Required*: No  
*Type*: [MSKAccessCredentials](aws-properties-pipes-pipe-mskaccesscredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumBatchingWindowInSeconds`  <a name="cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-maximumbatchingwindowinseconds"></a>
The maximum length of a time to wait for events\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartingPosition`  <a name="cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-startingposition"></a>
\(Streams only\) The position in a stream from which to start reading\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TopicName`  <a name="cfn-pipes-pipe-pipesourcemanagedstreamingkafkaparameters-topicname"></a>
The name of the topic that the pipe will read from\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)