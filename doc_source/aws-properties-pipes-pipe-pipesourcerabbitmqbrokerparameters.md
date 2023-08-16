# AWS::Pipes::Pipe PipeSourceRabbitMQBrokerParameters<a name="aws-properties-pipes-pipe-pipesourcerabbitmqbrokerparameters"></a>

The parameters for using a Rabbit MQ broker as a source\.

## Syntax<a name="aws-properties-pipes-pipe-pipesourcerabbitmqbrokerparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipesourcerabbitmqbrokerparameters-syntax.json"></a>

```
{
  "[BatchSize](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-batchsize)" : Integer,
  "[Credentials](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-credentials)" : MQBrokerAccessCredentials,
  "[MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-maximumbatchingwindowinseconds)" : Integer,
  "[QueueName](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-queuename)" : String,
  "[VirtualHost](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-virtualhost)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipesourcerabbitmqbrokerparameters-syntax.yaml"></a>

```
  [BatchSize](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-batchsize): Integer
  [Credentials](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-credentials): 
    MQBrokerAccessCredentials
  [MaximumBatchingWindowInSeconds](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-maximumbatchingwindowinseconds): Integer
  [QueueName](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-queuename): String
  [VirtualHost](#cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-virtualhost): String
```

## Properties<a name="aws-properties-pipes-pipe-pipesourcerabbitmqbrokerparameters-properties"></a>

`BatchSize`  <a name="cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-batchsize"></a>
The maximum number of records to include in each batch\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Credentials`  <a name="cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-credentials"></a>
The credentials needed to access the resource\.  
*Required*: Yes  
*Type*: [MQBrokerAccessCredentials](aws-properties-pipes-pipe-mqbrokeraccesscredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumBatchingWindowInSeconds`  <a name="cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-maximumbatchingwindowinseconds"></a>
The maximum length of a time to wait for events\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueName`  <a name="cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-queuename"></a>
The name of the destination queue to consume\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VirtualHost`  <a name="cfn-pipes-pipe-pipesourcerabbitmqbrokerparameters-virtualhost"></a>
The name of the virtual host associated with the source broker\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)