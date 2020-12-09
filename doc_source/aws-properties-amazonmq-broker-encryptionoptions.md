# AWS::AmazonMQ::Broker EncryptionOptions<a name="aws-properties-amazonmq-broker-encryptionoptions"></a>

Encryption options for the broker\.

**Important**  
Does not apply to RabbitMQ brokers\.

## Syntax<a name="aws-properties-amazonmq-broker-encryptionoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-encryptionoptions-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-amazonmq-broker-encryptionoptions-kmskeyid)" : String,
  "[UseAwsOwnedKey](#cfn-amazonmq-broker-encryptionoptions-useawsownedkey)" : Boolean
}
```

### YAML<a name="aws-properties-amazonmq-broker-encryptionoptions-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-amazonmq-broker-encryptionoptions-kmskeyid): String
  [UseAwsOwnedKey](#cfn-amazonmq-broker-encryptionoptions-useawsownedkey): Boolean
```

## Properties<a name="aws-properties-amazonmq-broker-encryptionoptions-properties"></a>

`KmsKeyId`  <a name="cfn-amazonmq-broker-encryptionoptions-kmskeyid"></a>
The customer master key \(CMK\) to use for the AWS Key Management Service \(KMS\)\. This key is used to encrypt your data at rest\. If not provided, Amazon MQ will use a default CMK to encrypt your data\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseAwsOwnedKey`  <a name="cfn-amazonmq-broker-encryptionoptions-useawsownedkey"></a>
Enables the use of an AWS owned CMK using AWS Key Management Service \(KMS\)\. Set to `true` by default, if no value is provided, for example, for RabbitMQ brokers\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)