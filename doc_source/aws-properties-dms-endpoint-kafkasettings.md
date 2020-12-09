# AWS::DMS::Endpoint KafkaSettings<a name="aws-properties-dms-endpoint-kafkasettings"></a>

Provides information that describes an Apache Kafka endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\.

## Syntax<a name="aws-properties-dms-endpoint-kafkasettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-kafkasettings-syntax.json"></a>

```
{
  "[Broker](#cfn-dms-endpoint-kafkasettings-broker)" : String,
  "[Topic](#cfn-dms-endpoint-kafkasettings-topic)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-kafkasettings-syntax.yaml"></a>

```
  [Broker](#cfn-dms-endpoint-kafkasettings-broker): String
  [Topic](#cfn-dms-endpoint-kafkasettings-topic): String
```

## Properties<a name="aws-properties-dms-endpoint-kafkasettings-properties"></a>

`Broker`  <a name="cfn-dms-endpoint-kafkasettings-broker"></a>
The broker location and port of the Kafka broker that hosts your Kafka instance\. Specify the broker in the form ` broker-hostname-or-ip:port `\. For example, `"ec2-12-345-678-901.compute-1.amazonaws.com:2345"`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Topic`  <a name="cfn-dms-endpoint-kafkasettings-topic"></a>
The topic to which you migrate the data\. If you don't specify a topic, AWS DMS specifies `"kafka-default-topic"` as the migration topic\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)