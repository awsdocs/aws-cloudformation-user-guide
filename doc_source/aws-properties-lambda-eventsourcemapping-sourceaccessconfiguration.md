# AWS::Lambda::EventSourceMapping SourceAccessConfiguration<a name="aws-properties-lambda-eventsourcemapping-sourceaccessconfiguration"></a>

An array of the authentication protocol, VPC components, or virtual host to secure and define your event source\.

## Syntax<a name="aws-properties-lambda-eventsourcemapping-sourceaccessconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-sourceaccessconfiguration-syntax.json"></a>

```
{
  "[Type](#cfn-lambda-eventsourcemapping-sourceaccessconfiguration-type)" : String,
  "[URI](#cfn-lambda-eventsourcemapping-sourceaccessconfiguration-uri)" : String
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-sourceaccessconfiguration-syntax.yaml"></a>

```
  [Type](#cfn-lambda-eventsourcemapping-sourceaccessconfiguration-type): String
  [URI](#cfn-lambda-eventsourcemapping-sourceaccessconfiguration-uri): String
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-sourceaccessconfiguration-properties"></a>

`Type`  <a name="cfn-lambda-eventsourcemapping-sourceaccessconfiguration-type"></a>
The type of authentication protocol, VPC components, or virtual host for your event source\. For example: `"Type":"SASL_SCRAM_512_AUTH"`\.  
+  `BASIC_AUTH` – \(Amazon MQ\) The AWS Secrets Manager secret that stores your broker credentials\.
+  `BASIC_AUTH` – \(Self\-managed Apache Kafka\) The Secrets Manager ARN of your secret key used for SASL/PLAIN authentication of your Apache Kafka brokers\.
+  `VPC_SUBNET` – \(Self\-managed Apache Kafka\) The subnets associated with your VPC\. Lambda connects to these subnets to fetch data from your self\-managed Apache Kafka cluster\.
+  `VPC_SECURITY_GROUP` – \(Self\-managed Apache Kafka\) The VPC security group used to manage access to your self\-managed Apache Kafka brokers\.
+  `SASL_SCRAM_256_AUTH` – \(Self\-managed Apache Kafka\) The Secrets Manager ARN of your secret key used for SASL SCRAM\-256 authentication of your self\-managed Apache Kafka brokers\.
+  `SASL_SCRAM_512_AUTH` – \(Amazon MSK, Self\-managed Apache Kafka\) The Secrets Manager ARN of your secret key used for SASL SCRAM\-512 authentication of your self\-managed Apache Kafka brokers\.
+  `VIRTUAL_HOST` –\- \(RabbitMQ\) The name of the virtual host in your RabbitMQ broker\. Lambda uses this RabbitMQ host as the event source\. This property cannot be specified in an UpdateEventSourceMapping API call\.
+  `CLIENT_CERTIFICATE_TLS_AUTH` – \(Amazon MSK, self\-managed Apache Kafka\) The Secrets Manager ARN of your secret key containing the certificate chain \(X\.509 PEM\), private key \(PKCS\#8 PEM\), and private key password \(optional\) used for mutual TLS authentication of your MSK/Apache Kafka brokers\.
+  `SERVER_ROOT_CA_CERTIFICATE` – \(Self\-managed Apache Kafka\) The Secrets Manager ARN of your secret key containing the root CA certificate \(X\.509 PEM\) used for TLS encryption of your Apache Kafka brokers\. 
*Required*: No  
*Type*: String  
*Allowed values*: `BASIC_AUTH | CLIENT_CERTIFICATE_TLS_AUTH | SASL_SCRAM_256_AUTH | SASL_SCRAM_512_AUTH | SERVER_ROOT_CA_CERTIFICATE | VIRTUAL_HOST | VPC_SECURITY_GROUP | VPC_SUBNET`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`URI`  <a name="cfn-lambda-eventsourcemapping-sourceaccessconfiguration-uri"></a>
The value for your chosen configuration in `Type`\. For example: `"URI": "arn:aws:secretsmanager:us-east-1:01234567890:secret:MyBrokerSecretName"`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `[a-zA-Z0-9-\/*:_+=.@-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)