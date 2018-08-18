# Amazon Kinesis Firehose DeliveryStream KMSEncryptionConfig<a name="aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig"></a>

The `KMSEncryptionConfig` property type specifies the AWS Key Management Service \(AWS KMS\) encryption key that Amazon Simple Storage Service \(Amazon S3\) uses to encrypt data delivered by the Amazon Kinesis Firehose \(Kinesis Firehose\) stream\.

`KMSEncryptionConfig` is a property of the [Amazon Kinesis Firehose DeliveryStream KMSEncryptionConfig](#aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig) property type\.

## Syntax<a name="aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig-syntax"></a>

### JSON<a name="aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig-syntax.json"></a>

```
{
  "[AWSKMSKeyARN](#cfn-kinesisfirehose-deliverystream-kmsencryptionconfig-awskmskeyarn)" : String
}
```

### YAML<a name="aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig-syntax.yaml"></a>

```
[AWSKMSKeyARN](#cfn-kinesisfirehose-deliverystream-kmsencryptionconfig-awskmskeyarn): String
```

## Properties<a name="aws-properties-kinesisfirehose-deliverystream-kmsencryptionconfig-properties"></a>

`AWSKMSKeyARN`  <a name="cfn-kinesisfirehose-deliverystream-kmsencryptionconfig-awskmskeyarn"></a>
The Amazon Resource Name \(ARN\) of the AWS KMS encryption key that Amazon S3 uses to encrypt data delivered by the Kinesis Firehose stream\. The key must belong to the same region as the destination S3 bucket\.  
*Required*: Yes  
*Type*: String