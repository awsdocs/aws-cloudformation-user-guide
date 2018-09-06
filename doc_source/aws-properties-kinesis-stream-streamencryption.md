# Kinesis StreamEncryption<a name="aws-properties-kinesis-stream-streamencryption"></a>

The `StreamEncryption` property is part of the [AWS::Kinesis::Stream](aws-resource-kinesis-stream.md) resource that enables or updates server\-side encryption using an AWS KMS key for a specified stream\. For more information, see [StartStreamEncryption](http://docs.aws.amazon.com/kinesis/latest/APIReference/API_StartStreamEncryption.html) in the *Amazon Kinesis Data Streams API Reference*\.

## Syntax<a name="w3ab2c21c14e1393b5"></a>

### JSON<a name="aws-properties-kinesis-stream-streamencryption.json"></a>

```
{
  "[EncryptionType](#cfn-kinesis-stream-streamencryption-encryptiontype)" : String,
  "[KeyId](#cfn-kinesis-stream-streamencryption-keyid)" : String
}
```

### YAML<a name="aws-properties-kinesis-stream-streamencryption.yaml"></a>

```
[EncryptionType](#cfn-kinesis-stream-streamencryption-encryptiontype): String
[KeyId](#cfn-kinesis-stream-streamencryption-keyid): String
```

## Properties<a name="w3ab2c21c14e1393b7"></a>

`EncryptionType`  <a name="cfn-kinesis-stream-streamencryption-encryptiontype"></a>
The encryption type to use\. The only valid value is `KMS`\.  
*Required*: Yes  
*Type*: String

`KeyId`  <a name="cfn-kinesis-stream-streamencryption-keyid"></a>
The GUID for the customer\-managed KMS key to use for encryption\. This value can be a globally unique identifier, a fully specified ARN to either an alias or a key, or an alias name prefixed by "alias/"\. You can also use a master key owned by Kinesis Streams by specifying the alias `aws/kinesis`\.  
+ Key ARN example: arn:aws: `kms:us-east-1:123456789012:key/12345678-1234-1234-1234-123456789012`
+ Alias ARN example: `arn:aws:kms:us-east-1:123456789012:alias/MyAliasName`
+ Globally unique key ID example: `12345678-1234-1234-1234-123456789012`
+ Alias name example: `alias/MyAliasName`
+ Master key owned by Kinesis Streams: `alias/aws/kinesis`
*Required*: Yes  
*Type*: String