# AWS::Kinesis::Stream StreamEncryption<a name="aws-properties-kinesis-stream-streamencryption"></a>

Enables or updates server\-side encryption using an AWS KMS key for a specified stream\. 

Starting encryption is an asynchronous operation\. Upon receiving the request, Kinesis Data Streams returns immediately and sets the status of the stream to `UPDATING`\. After the update is complete, Kinesis Data Streams sets the status of the stream back to `ACTIVE`\. Updating or applying encryption normally takes a few seconds to complete, but it can take minutes\. You can continue to read and write data to your stream while its status is `UPDATING`\. Once the status of the stream is `ACTIVE`, encryption begins for records written to the stream\. 

API Limits: You can successfully apply a new AWS KMS key for server\-side encryption 25 times in a rolling 24\-hour period\.

Note: It can take up to 5 seconds after the stream is in an `ACTIVE` status before all records written to the stream are encrypted\. After you enable encryption, you can verify that encryption is applied by inspecting the API response from `PutRecord` or `PutRecords`\.

## Syntax<a name="aws-properties-kinesis-stream-streamencryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesis-stream-streamencryption-syntax.json"></a>

```
{
  "[EncryptionType](#cfn-kinesis-stream-streamencryption-encryptiontype)" : String,
  "[KeyId](#cfn-kinesis-stream-streamencryption-keyid)" : String
}
```

### YAML<a name="aws-properties-kinesis-stream-streamencryption-syntax.yaml"></a>

```
  [EncryptionType](#cfn-kinesis-stream-streamencryption-encryptiontype): String
  [KeyId](#cfn-kinesis-stream-streamencryption-keyid): String
```

## Properties<a name="aws-properties-kinesis-stream-streamencryption-properties"></a>

`EncryptionType`  <a name="cfn-kinesis-stream-streamencryption-encryptiontype"></a>
The encryption type to use\. The only valid value is `KMS`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyId`  <a name="cfn-kinesis-stream-streamencryption-keyid"></a>
The GUID for the customer\-managed AWS KMS key to use for encryption\. This value can be a globally unique identifier, a fully specified Amazon Resource Name \(ARN\) to either an alias or a key, or an alias name prefixed by "alias/"\.You can also use a master key owned by Kinesis Data Streams by specifying the alias `aws/kinesis`\.  
+ Key ARN example: `arn:aws:kms:us-east-1:123456789012:key/12345678-1234-1234-1234-123456789012` 
+ Alias ARN example: `arn:aws:kms:us-east-1:123456789012:alias/MyAliasName` 
+ Globally unique key ID example: `12345678-1234-1234-1234-123456789012` 
+ Alias name example: `alias/MyAliasName` 
+ Master key owned by Kinesis Data Streams: `alias/aws/kinesis` 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)