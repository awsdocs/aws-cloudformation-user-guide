# AWS::KafkaConnect::Connector ProvisionedCapacity<a name="aws-properties-kafkaconnect-connector-provisionedcapacity"></a>

Details about a connector's provisioned capacity\.

## Syntax<a name="aws-properties-kafkaconnect-connector-provisionedcapacity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-provisionedcapacity-syntax.json"></a>

```
{
  "[McuCount](#cfn-kafkaconnect-connector-provisionedcapacity-mcucount)" : Integer,
  "[WorkerCount](#cfn-kafkaconnect-connector-provisionedcapacity-workercount)" : Integer
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-provisionedcapacity-syntax.yaml"></a>

```
  [McuCount](#cfn-kafkaconnect-connector-provisionedcapacity-mcucount): Integer
  [WorkerCount](#cfn-kafkaconnect-connector-provisionedcapacity-workercount): Integer
```

## Properties<a name="aws-properties-kafkaconnect-connector-provisionedcapacity-properties"></a>

`McuCount`  <a name="cfn-kafkaconnect-connector-provisionedcapacity-mcucount"></a>
The number of microcontroller units \(MCUs\) allocated to each connector worker\. The valid values are 1,2,4,8\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkerCount`  <a name="cfn-kafkaconnect-connector-provisionedcapacity-workercount"></a>
The number of workers that are allocated to the connector\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)