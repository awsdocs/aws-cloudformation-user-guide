# AWS::KafkaConnect::Connector<a name="aws-resource-kafkaconnect-connector"></a>

Creates a connector using the specified properties\. 

## Syntax<a name="aws-resource-kafkaconnect-connector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kafkaconnect-connector-syntax.json"></a>

```
{
  "Type" : "AWS::KafkaConnect::Connector",
  "Properties" : {
      "[Capacity](#cfn-kafkaconnect-connector-capacity)" : Capacity,
      "[ConnectorConfiguration](#cfn-kafkaconnect-connector-connectorconfiguration)" : {Key : Value, ...},
      "[ConnectorDescription](#cfn-kafkaconnect-connector-connectordescription)" : String,
      "[ConnectorName](#cfn-kafkaconnect-connector-connectorname)" : String,
      "[KafkaCluster](#cfn-kafkaconnect-connector-kafkacluster)" : KafkaCluster,
      "[KafkaClusterClientAuthentication](#cfn-kafkaconnect-connector-kafkaclusterclientauthentication)" : KafkaClusterClientAuthentication,
      "[KafkaClusterEncryptionInTransit](#cfn-kafkaconnect-connector-kafkaclusterencryptionintransit)" : KafkaClusterEncryptionInTransit,
      "[KafkaConnectVersion](#cfn-kafkaconnect-connector-kafkaconnectversion)" : String,
      "[LogDelivery](#cfn-kafkaconnect-connector-logdelivery)" : LogDelivery,
      "[Plugins](#cfn-kafkaconnect-connector-plugins)" : [ Plugin, ... ],
      "[ServiceExecutionRoleArn](#cfn-kafkaconnect-connector-serviceexecutionrolearn)" : String,
      "[WorkerConfiguration](#cfn-kafkaconnect-connector-workerconfiguration)" : WorkerConfiguration
    }
}
```

### YAML<a name="aws-resource-kafkaconnect-connector-syntax.yaml"></a>

```
Type: AWS::KafkaConnect::Connector
Properties: 
  [Capacity](#cfn-kafkaconnect-connector-capacity): 
    Capacity
  [ConnectorConfiguration](#cfn-kafkaconnect-connector-connectorconfiguration): 
    Key : Value
  [ConnectorDescription](#cfn-kafkaconnect-connector-connectordescription): String
  [ConnectorName](#cfn-kafkaconnect-connector-connectorname): String
  [KafkaCluster](#cfn-kafkaconnect-connector-kafkacluster): 
    KafkaCluster
  [KafkaClusterClientAuthentication](#cfn-kafkaconnect-connector-kafkaclusterclientauthentication): 
    KafkaClusterClientAuthentication
  [KafkaClusterEncryptionInTransit](#cfn-kafkaconnect-connector-kafkaclusterencryptionintransit): 
    KafkaClusterEncryptionInTransit
  [KafkaConnectVersion](#cfn-kafkaconnect-connector-kafkaconnectversion): String
  [LogDelivery](#cfn-kafkaconnect-connector-logdelivery): 
    LogDelivery
  [Plugins](#cfn-kafkaconnect-connector-plugins): 
    - Plugin
  [ServiceExecutionRoleArn](#cfn-kafkaconnect-connector-serviceexecutionrolearn): String
  [WorkerConfiguration](#cfn-kafkaconnect-connector-workerconfiguration): 
    WorkerConfiguration
```

## Properties<a name="aws-resource-kafkaconnect-connector-properties"></a>

`Capacity`  <a name="cfn-kafkaconnect-connector-capacity"></a>
The connector's compute capacity settings\.  
*Required*: Yes  
*Type*: [Capacity](aws-properties-kafkaconnect-connector-capacity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectorConfiguration`  <a name="cfn-kafkaconnect-connector-connectorconfiguration"></a>
The configuration of the connector\.  
*Required*: Yes  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectorDescription`  <a name="cfn-kafkaconnect-connector-connectordescription"></a>
The description of the connector\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectorName`  <a name="cfn-kafkaconnect-connector-connectorname"></a>
The name of the connector\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KafkaCluster`  <a name="cfn-kafkaconnect-connector-kafkacluster"></a>
The details of the Apache Kafka cluster to which the connector is connected\.  
*Required*: Yes  
*Type*: [KafkaCluster](aws-properties-kafkaconnect-connector-kafkacluster.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KafkaClusterClientAuthentication`  <a name="cfn-kafkaconnect-connector-kafkaclusterclientauthentication"></a>
The type of client authentication used to connect to the Apache Kafka cluster\. The value is NONE when no client authentication is used\.  
*Required*: Yes  
*Type*: [KafkaClusterClientAuthentication](aws-properties-kafkaconnect-connector-kafkaclusterclientauthentication.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KafkaClusterEncryptionInTransit`  <a name="cfn-kafkaconnect-connector-kafkaclusterencryptionintransit"></a>
Details of encryption in transit to the Apache Kafka cluster\.  
*Required*: Yes  
*Type*: [KafkaClusterEncryptionInTransit](aws-properties-kafkaconnect-connector-kafkaclusterencryptionintransit.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KafkaConnectVersion`  <a name="cfn-kafkaconnect-connector-kafkaconnectversion"></a>
The version of Kafka Connect\. It has to be compatible with both the Apache Kafka cluster's version and the plugins\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogDelivery`  <a name="cfn-kafkaconnect-connector-logdelivery"></a>
The settings for delivering connector logs to Amazon CloudWatch Logs\.  
*Required*: No  
*Type*: [LogDelivery](aws-properties-kafkaconnect-connector-logdelivery.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Plugins`  <a name="cfn-kafkaconnect-connector-plugins"></a>
Specifies which plugin to use for the connector\. You must specify a single\-element list\. Amazon MSK Connect does not currently support specifying multiple plugins\.  
*Required*: Yes  
*Type*: List of [Plugin](aws-properties-kafkaconnect-connector-plugin.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceExecutionRoleArn`  <a name="cfn-kafkaconnect-connector-serviceexecutionrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used by the connector to access Amazon Web Services resources\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WorkerConfiguration`  <a name="cfn-kafkaconnect-connector-workerconfiguration"></a>
The worker configurations that are in use with the connector\.  
*Required*: No  
*Type*: [WorkerConfiguration](aws-properties-kafkaconnect-connector-workerconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-kafkaconnect-connector-return-values"></a>

### Ref<a name="aws-resource-kafkaconnect-connector-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-kafkaconnect-connector-return-values-fn--getatt"></a>

#### <a name="aws-resource-kafkaconnect-connector-return-values-fn--getatt-fn--getatt"></a>

`ConnectorArn`  <a name="ConnectorArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the newly created connector\.