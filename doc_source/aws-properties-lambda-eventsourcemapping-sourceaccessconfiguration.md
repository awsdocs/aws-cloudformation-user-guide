# AWS::Lambda::EventSourceMapping SourceAccessConfiguration<a name="aws-properties-lambda-eventsourcemapping-sourceaccessconfiguration"></a>

An array of the authentication protocol, or the VPC components to secure your event source\. To encrypt the secret, you can use customer or service managed keys\. When using a customer managed KMS key, the Lambda execution role requires kms:Decrypt permissions\.

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
The type of authentication protocol or the VPC components for your event source. For example: `SASL_SCRAM_512_AUTH` .

- `BASIC_AUTH` - (MQ) The Secrets Manager secret that stores your broker credentials.
- `VPC_SUBNET` - The subnets associated with your VPC. Lambda connects to these subnets to fetch data from your Kafka cluster.
- `VPC_SECURITY_GROUP` - The VPC security group used to manage access to your Kafka brokers.
- `SASL_SCRAM_256_AUTH` - The ARN of your secret key used for SASL SCRAM-256 authentication of your Kafka brokers.
- `SASL_SCRAM_512_AUTH` - The ARN of your secret key used for SASL SCRAM-512 authentication of your Kafka brokers.

*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`URI`  <a name="cfn-lambda-eventsourcemapping-sourceaccessconfiguration-uri"></a>
The ARN of the AWS Secrets Manager secret\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
