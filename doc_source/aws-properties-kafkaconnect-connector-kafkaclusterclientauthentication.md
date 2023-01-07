# AWS::KafkaConnect::Connector KafkaClusterClientAuthentication<a name="aws-properties-kafkaconnect-connector-kafkaclusterclientauthentication"></a>

The client authentication information used in order to authenticate with the Apache Kafka cluster\.

## Syntax<a name="aws-properties-kafkaconnect-connector-kafkaclusterclientauthentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-kafkaclusterclientauthentication-syntax.json"></a>

```
{
  "[AuthenticationType](#cfn-kafkaconnect-connector-kafkaclusterclientauthentication-authenticationtype)" : String
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-kafkaclusterclientauthentication-syntax.yaml"></a>

```
  [AuthenticationType](#cfn-kafkaconnect-connector-kafkaclusterclientauthentication-authenticationtype): String
```

## Properties<a name="aws-properties-kafkaconnect-connector-kafkaclusterclientauthentication-properties"></a>

`AuthenticationType`  <a name="cfn-kafkaconnect-connector-kafkaclusterclientauthentication-authenticationtype"></a>
The type of client authentication used to connect to the Apache Kafka cluster\. Value NONE means that no client authentication is used\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)