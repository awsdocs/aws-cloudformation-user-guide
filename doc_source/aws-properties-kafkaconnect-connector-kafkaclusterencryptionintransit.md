# AWS::KafkaConnect::Connector KafkaClusterEncryptionInTransit<a name="aws-properties-kafkaconnect-connector-kafkaclusterencryptionintransit"></a>

Details of encryption in transit to the Apache Kafka cluster\.

## Syntax<a name="aws-properties-kafkaconnect-connector-kafkaclusterencryptionintransit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-kafkaclusterencryptionintransit-syntax.json"></a>

```
{
  "[EncryptionType](#cfn-kafkaconnect-connector-kafkaclusterencryptionintransit-encryptiontype)" : String
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-kafkaclusterencryptionintransit-syntax.yaml"></a>

```
  [EncryptionType](#cfn-kafkaconnect-connector-kafkaclusterencryptionintransit-encryptiontype): String
```

## Properties<a name="aws-properties-kafkaconnect-connector-kafkaclusterencryptionintransit-properties"></a>

`EncryptionType`  <a name="cfn-kafkaconnect-connector-kafkaclusterencryptionintransit-encryptiontype"></a>
The type of encryption in transit to the Apache Kafka cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)