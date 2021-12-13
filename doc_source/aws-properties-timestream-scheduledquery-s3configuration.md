# AWS::Timestream::ScheduledQuery S3Configuration<a name="aws-properties-timestream-scheduledquery-s3configuration"></a>

Details on S3 location for error reports that result from running a query\. 

## Syntax<a name="aws-properties-timestream-scheduledquery-s3configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-scheduledquery-s3configuration-syntax.json"></a>

```
{
  "[BucketName](#cfn-timestream-scheduledquery-s3configuration-bucketname)" : String,
  "[EncryptionOption](#cfn-timestream-scheduledquery-s3configuration-encryptionoption)" : String,
  "[ObjectKeyPrefix](#cfn-timestream-scheduledquery-s3configuration-objectkeyprefix)" : String
}
```

### YAML<a name="aws-properties-timestream-scheduledquery-s3configuration-syntax.yaml"></a>

```
  [BucketName](#cfn-timestream-scheduledquery-s3configuration-bucketname): String
  [EncryptionOption](#cfn-timestream-scheduledquery-s3configuration-encryptionoption): String
  [ObjectKeyPrefix](#cfn-timestream-scheduledquery-s3configuration-objectkeyprefix): String
```

## Properties<a name="aws-properties-timestream-scheduledquery-s3configuration-properties"></a>

`BucketName`  <a name="cfn-timestream-scheduledquery-s3configuration-bucketname"></a>
 Name of the S3 bucket under which error reports will be created\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9]`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EncryptionOption`  <a name="cfn-timestream-scheduledquery-s3configuration-encryptionoption"></a>
 Encryption at rest options for the error reports\. If no encryption option is specified, Timestream will choose SSE\_S3 as default\.   
*Required*: No  
*Type*: String  
*Allowed values*: `SSE_KMS | SSE_S3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ObjectKeyPrefix`  <a name="cfn-timestream-scheduledquery-s3configuration-objectkeyprefix"></a>
 Prefix for the error report key\. Timestream by default adds the following prefix to the error report path\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `928`  
*Pattern*: `[a-zA-Z0-9|!\-_*'\(\)]([a-zA-Z0-9]|[!\-_*'\(\)\/.])+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)