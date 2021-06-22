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
A comma\-separated list of one or more broker locations in your Kafka cluster that host your Kafka instance\. Specify each broker location in the form ` broker-hostname-or-ip:port `\. For example, `"ec2-12-345-678-901.compute-1.amazonaws.com:2345"`\. For more information and examples of specifying a list of broker locations, see [Using Apache Kafka as a target for AWS Database Migration Service ](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Kafka.html) in the * AWS Database Migration Service User Guide*\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Topic`  <a name="cfn-dms-endpoint-kafkasettings-topic"></a>
The topic to which you migrate the data\. If you don't specify a topic, AWS DMS specifies `"kafka-default-topic"` as the migration topic\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)