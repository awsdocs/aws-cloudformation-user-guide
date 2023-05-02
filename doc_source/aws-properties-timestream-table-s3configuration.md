# AWS::Timestream::Table S3Configuration<a name="aws-properties-timestream-table-s3configuration"></a>

The configuration that specifies an S3 location\.

## Syntax<a name="aws-properties-timestream-table-s3configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-table-s3configuration-syntax.json"></a>

```
{
  "[BucketName](#cfn-timestream-table-s3configuration-bucketname)" : String,
  "[EncryptionOption](#cfn-timestream-table-s3configuration-encryptionoption)" : String,
  "[KmsKeyId](#cfn-timestream-table-s3configuration-kmskeyid)" : String,
  "[ObjectKeyPrefix](#cfn-timestream-table-s3configuration-objectkeyprefix)" : String
}
```

### YAML<a name="aws-properties-timestream-table-s3configuration-syntax.yaml"></a>

```
  [BucketName](#cfn-timestream-table-s3configuration-bucketname): String
  [EncryptionOption](#cfn-timestream-table-s3configuration-encryptionoption): String
  [KmsKeyId](#cfn-timestream-table-s3configuration-kmskeyid): String
  [ObjectKeyPrefix](#cfn-timestream-table-s3configuration-objectkeyprefix): String
```

## Properties<a name="aws-properties-timestream-table-s3configuration-properties"></a>

`BucketName`  <a name="cfn-timestream-table-s3configuration-bucketname"></a>
The bucket name of the customer S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionOption`  <a name="cfn-timestream-table-s3configuration-encryptionoption"></a>
The encryption option for the customer S3 location\. Options are S3 server\-side encryption with an S3 managed key or AWS managed key\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SSE_KMS | SSE_S3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-timestream-table-s3configuration-kmskeyid"></a>
The AWS KMS key ID for the customer S3 location when encrypting with an AWS managed key\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectKeyPrefix`  <a name="cfn-timestream-table-s3configuration-objectkeyprefix"></a>
The object key preview for the customer S3 location\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `928`  
*Pattern*: `[a-zA-Z0-9|!\-_*'\(\)]([a-zA-Z0-9]|[!\-_*'\(\)\/.])+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)