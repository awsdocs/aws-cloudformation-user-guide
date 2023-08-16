# AWS::Pipes::Pipe PipeSourceActiveMQBrokerParameters<a name="aws-properties-pipes-pipe-pipesourceactivemqbrokerparameters"></a>

The parameters for using an Active MQ broker as a source\.

## Syntax<a name="aws-properties-pipes-pipe-pipesourceactivemqbrokerparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipesourceactivemqbrokerparameters-syntax.json"></a>

```
{
  "[BatchSize](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-batchsize)" : Integer,
  "[Credentials](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-credentials)" : MQBrokerAccessCredentials,
  "[MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-maximumbatchingwindowinseconds)" : Integer,
  "[QueueName](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-queuename)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipesourceactivemqbrokerparameters-syntax.yaml"></a>

```
  [BatchSize](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-batchsize): Integer
  [Credentials](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-credentials): 
    MQBrokerAccessCredentials
  [MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-maximumbatchingwindowinseconds): Integer
  [QueueName](#cfn-pipes-pipe-pipesourceactivemqbrokerparameters-queuename): String
```

## Properties<a name="aws-properties-pipes-pipe-pipesourceactivemqbrokerparameters-properties"></a>

`BatchSize`  <a name="cfn-pipes-pipe-pipesourceactivemqbrokerparameters-batchsize"></a>
The maximum number of records to include in each batch\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Credentials`  <a name="cfn-pipes-pipe-pipesourceactivemqbrokerparameters-credentials"></a>
The credentials needed to access the resource\.  
*Required*: Yes  
*Type*: [MQBrokerAccessCredentials](aws-properties-pipes-pipe-mqbrokeraccesscredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumBatchingWindowInSeconds`  <a name="cfn-pipes-pipe-pipesourceactivemqbrokerparameters-maximumbatchingwindowinseconds"></a>
The maximum length of a time to wait for events\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueName`  <a name="cfn-pipes-pipe-pipesourceactivemqbrokerparameters-queuename"></a>
The name of the destination queue to consume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)