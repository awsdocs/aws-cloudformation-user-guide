# AWS::KinesisFirehose::DeliveryStream EncryptionConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration"></a>

The `EncryptionConfiguration` property type specifies the encryption settings that Amazon Kinesis Data Firehose \(Kinesis Data Firehose\) uses when delivering data to Amazon Simple Storage Service \(Amazon S3\)\. 

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-syntax.json"></a>

```
{
  "[KMSEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-kmsencryptionconfig)" : KMSEncryptionConfig,
  "[NoEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-noencryptionconfig)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-syntax.yaml"></a>

```
  [KMSEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-kmsencryptionconfig): 
    KMSEncryptionConfig
  [NoEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-noencryptionconfig): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-properties"></a>

`KMSEncryptionConfig`  <a name="cfn-kinesisfirehose-deliverystream-encryptionconfiguration-kmsencryptionconfig"></a>
The AWS Key Management Service \(AWS KMS\) encryption key that Amazon S3 uses to encrypt your data\.   
*Required*: No  
*Type*: [KMSEncryptionConfig](aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NoEncryptionConfig`  <a name="cfn-kinesisfirehose-deliverystream-encryptionconfiguration-noencryptionconfig"></a>
Disables encryption\. For valid values, see the `NoEncryptionConfig` content for the [EncryptionConfiguration](https://docs.aws.amazon.com/firehose/latest/APIReference/API_EncryptionConfiguration.html) data type in the *Amazon Kinesis Data Firehose API Reference*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `NoEncryption`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)