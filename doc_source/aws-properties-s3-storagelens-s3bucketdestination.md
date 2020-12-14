# AWS::S3::StorageLens S3BucketDestination<a name="aws-properties-s3-storagelens-s3bucketdestination"></a>

This resource contains the details of the bucket where the Amazon S3 Storage Lens metrics export will be placed\.

## Syntax<a name="aws-properties-s3-storagelens-s3bucketdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-storagelens-s3bucketdestination-syntax.json"></a>

```
{
  "[AccountId](#cfn-s3-storagelens-s3bucketdestination-accountid)" : String,
  "[Arn](#cfn-s3-storagelens-s3bucketdestination-arn)" : String,
  "[Encryption](#cfn-s3-storagelens-s3bucketdestination-encryption)" : Encryption,
  "[Format](#cfn-s3-storagelens-s3bucketdestination-format)" : String,
  "[OutputSchemaVersion](#cfn-s3-storagelens-s3bucketdestination-outputschemaversion)" : String,
  "[Prefix](#cfn-s3-storagelens-s3bucketdestination-prefix)" : String
}
```

### YAML<a name="aws-properties-s3-storagelens-s3bucketdestination-syntax.yaml"></a>

```
  [AccountId](#cfn-s3-storagelens-s3bucketdestination-accountid): String
  [Arn](#cfn-s3-storagelens-s3bucketdestination-arn): String
  [Encryption](#cfn-s3-storagelens-s3bucketdestination-encryption): 
    Encryption
  [Format](#cfn-s3-storagelens-s3bucketdestination-format): String
  [OutputSchemaVersion](#cfn-s3-storagelens-s3bucketdestination-outputschemaversion): String
  [Prefix](#cfn-s3-storagelens-s3bucketdestination-prefix): String
```

## Properties<a name="aws-properties-s3-storagelens-s3bucketdestination-properties"></a>

`AccountId`  <a name="cfn-s3-storagelens-s3bucketdestination-accountid"></a>
This property contains the details of the AWS account ID of the S3 Storage Lens export bucket destination\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Arn`  <a name="cfn-s3-storagelens-s3bucketdestination-arn"></a>
This property contains the details of the ARN of the bucket destination of the S3 Storage Lens export \.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Encryption`  <a name="cfn-s3-storagelens-s3bucketdestination-encryption"></a>
This property contains the details of the encryption of the bucket destination of the Amazon S3 Storage Lens metrics export\.  
*Required*: No  
*Type*: [Encryption](aws-properties-s3-storagelens-encryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Format`  <a name="cfn-s3-storagelens-s3bucketdestination-format"></a>
This property contains the details of the format of the S3 Storage Lens export bucket destination\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputSchemaVersion`  <a name="cfn-s3-storagelens-s3bucketdestination-outputschemaversion"></a>
This property contains the details of the output schema version of the S3 Storage Lens export bucket destination\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-storagelens-s3bucketdestination-prefix"></a>
This property contains the details of the prefix of the bucket destination of the S3 Storage Lens export \.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)