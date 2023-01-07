# AWS::KafkaConnect::Connector KafkaCluster<a name="aws-properties-kafkaconnect-connector-kafkacluster"></a>

The details of the Apache Kafka cluster to which the connector is connected\.

## Syntax<a name="aws-properties-kafkaconnect-connector-kafkacluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-kafkacluster-syntax.json"></a>

```
{
  "[ApacheKafkaCluster](#cfn-kafkaconnect-connector-kafkacluster-apachekafkacluster)" : ApacheKafkaCluster
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-kafkacluster-syntax.yaml"></a>

```
  [ApacheKafkaCluster](#cfn-kafkaconnect-connector-kafkacluster-apachekafkacluster): 
    ApacheKafkaCluster
```

## Properties<a name="aws-properties-kafkaconnect-connector-kafkacluster-properties"></a>

`ApacheKafkaCluster`  <a name="cfn-kafkaconnect-connector-kafkacluster-apachekafkacluster"></a>
The Apache Kafka cluster to which the connector is connected\.  
*Required*: Yes  
*Type*: [ApacheKafkaCluster](aws-properties-kafkaconnect-connector-apachekafkacluster.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)