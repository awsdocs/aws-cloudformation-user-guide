# AWS::SSM::ResourceDataSync S3Destination<a name="aws-properties-ssm-resourcedatasync-s3destination"></a>

Information about the target S3 bucket for the Resource Data Sync\.

## Syntax<a name="aws-properties-ssm-resourcedatasync-s3destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-resourcedatasync-s3destination-syntax.json"></a>

```
{
  "[BucketName](#cfn-ssm-resourcedatasync-s3destination-bucketname)" : String,
  "[BucketPrefix](#cfn-ssm-resourcedatasync-s3destination-bucketprefix)" : String,
  "[BucketRegion](#cfn-ssm-resourcedatasync-s3destination-bucketregion)" : String,
  "[KMSKeyArn](#cfn-ssm-resourcedatasync-s3destination-kmskeyarn)" : String,
  "[SyncFormat](#cfn-ssm-resourcedatasync-s3destination-syncformat)" : String
}
```

### YAML<a name="aws-properties-ssm-resourcedatasync-s3destination-syntax.yaml"></a>

```
  [BucketName](#cfn-ssm-resourcedatasync-s3destination-bucketname): String
  [BucketPrefix](#cfn-ssm-resourcedatasync-s3destination-bucketprefix): String
  [BucketRegion](#cfn-ssm-resourcedatasync-s3destination-bucketregion): String
  [KMSKeyArn](#cfn-ssm-resourcedatasync-s3destination-kmskeyarn): String
  [SyncFormat](#cfn-ssm-resourcedatasync-s3destination-syncformat): String
```

## Properties<a name="aws-properties-ssm-resourcedatasync-s3destination-properties"></a>

`BucketName`  <a name="cfn-ssm-resourcedatasync-s3destination-bucketname"></a>
The name of the S3 bucket where the aggregated data is stored\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketPrefix`  <a name="cfn-ssm-resourcedatasync-s3destination-bucketprefix"></a>
An Amazon S3 prefix for the bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketRegion`  <a name="cfn-ssm-resourcedatasync-s3destination-bucketregion"></a>
The AWS Region with the S3 bucket targeted by the Resource Data Sync\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KMSKeyArn`  <a name="cfn-ssm-resourcedatasync-s3destination-kmskeyarn"></a>
The ARN of an encryption key for a destination in Amazon S3\. Must belong to the same Region as the destination S3 bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SyncFormat`  <a name="cfn-ssm-resourcedatasync-s3destination-syncformat"></a>
A supported sync format\. The following format is currently supported: JsonSerDe  
*Required*: Yes  
*Type*: String  
*Allowed values*: `JsonSerDe`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)