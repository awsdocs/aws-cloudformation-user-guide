# Amazon Kinesis Firehose DeliveryStream EncryptionConfiguration<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration"></a>

The `EncryptionConfiguration` property type specifies the encryption settings that Amazon Kinesis Firehose \(Kinesis Firehose\) uses when delivering data to Amazon Simple Storage Service \(Amazon S3\)\.

`EncryptionConfiguration` is a property of the [Amazon Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md) property type\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-syntax.json"></a>

```
{
  "[KMSEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-kmsencryptionconfig)" : [KMSEncryptionConfig](aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig.md),
  "[NoEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-noencryptionconfig)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-syntax.yaml"></a>

```
[KMSEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-kmsencryptionconfig):
  [KMSEncryptionConfig](aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig.md)
[NoEncryptionConfig](#cfn-kinesisfirehose-deliverystream-encryptionconfiguration-noencryptionconfig): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-encryptionconfiguration-properties"></a>

`KMSEncryptionConfig`  <a name="cfn-kinesisfirehose-deliverystream-encryptionconfiguration-kmsencryptionconfig"></a>
The AWS Key Management Service \(AWS KMS\) encryption key that Amazon S3 uses to encrypt your data\.  
*Required*: No  
*Type*: [Amazon Kinesis Firehose DeliveryStream KMSEncryptionConfig](aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig.md)

`NoEncryptionConfig`  <a name="cfn-kinesisfirehose-deliverystream-encryptionconfiguration-noencryptionconfig"></a>
Disables encryption\. For valid values, see the `NoEncryptionConfig` content for the [EncryptionConfiguration](http://docs.aws.amazon.com/firehose/latest/APIReference/API_EncryptionConfiguration.html) data type in the *Amazon Kinesis Firehose API Reference*\.  
*Required*: No  
*Type*: String