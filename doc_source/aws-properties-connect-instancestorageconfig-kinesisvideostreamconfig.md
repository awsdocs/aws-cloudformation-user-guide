# AWS::Connect::InstanceStorageConfig KinesisVideoStreamConfig<a name="aws-properties-connect-instancestorageconfig-kinesisvideostreamconfig"></a>

Configuration information of a Kinesis video stream\.

## Syntax<a name="aws-properties-connect-instancestorageconfig-kinesisvideostreamconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-instancestorageconfig-kinesisvideostreamconfig-syntax.json"></a>

```
{
  "[EncryptionConfig](#cfn-connect-instancestorageconfig-kinesisvideostreamconfig-encryptionconfig)" : EncryptionConfig,
  "[Prefix](#cfn-connect-instancestorageconfig-kinesisvideostreamconfig-prefix)" : String,
  "[RetentionPeriodHours](#cfn-connect-instancestorageconfig-kinesisvideostreamconfig-retentionperiodhours)" : Double
}
```

### YAML<a name="aws-properties-connect-instancestorageconfig-kinesisvideostreamconfig-syntax.yaml"></a>

```
  [EncryptionConfig](#cfn-connect-instancestorageconfig-kinesisvideostreamconfig-encryptionconfig): 
    EncryptionConfig
  [Prefix](#cfn-connect-instancestorageconfig-kinesisvideostreamconfig-prefix): String
  [RetentionPeriodHours](#cfn-connect-instancestorageconfig-kinesisvideostreamconfig-retentionperiodhours): Double
```

## Properties<a name="aws-properties-connect-instancestorageconfig-kinesisvideostreamconfig-properties"></a>

`EncryptionConfig`  <a name="cfn-connect-instancestorageconfig-kinesisvideostreamconfig-encryptionconfig"></a>
The encryption configuration\.  
*Required*: No  
*Type*: [EncryptionConfig](aws-properties-connect-instancestorageconfig-encryptionconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-connect-instancestorageconfig-kinesisvideostreamconfig-prefix"></a>
The prefix of the video stream\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetentionPeriodHours`  <a name="cfn-connect-instancestorageconfig-kinesisvideostreamconfig-retentionperiodhours"></a>
The number of hours data is retained in the stream\. Kinesis Video Streams retains the data in a data store that is associated with the stream\.  
The default value is 0, indicating that the stream does not persist data\.  
*Required*: Yes  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `87600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)