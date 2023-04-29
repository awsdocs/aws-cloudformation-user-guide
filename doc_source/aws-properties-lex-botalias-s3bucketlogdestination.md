# AWS::Lex::BotAlias S3BucketLogDestination<a name="aws-properties-lex-botalias-s3bucketlogdestination"></a>

<a name="aws-properties-lex-botalias-s3bucketlogdestination-description"></a>The `S3BucketLogDestination` property type specifies Property description not available\. for an [AWS::Lex::BotAlias](aws-resource-lex-botalias.md)\.

## Syntax<a name="aws-properties-lex-botalias-s3bucketlogdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-s3bucketlogdestination-syntax.json"></a>

```
{
  "[KmsKeyArn](#cfn-lex-botalias-s3bucketlogdestination-kmskeyarn)" : String,
  "[LogPrefix](#cfn-lex-botalias-s3bucketlogdestination-logprefix)" : String,
  "[S3BucketArn](#cfn-lex-botalias-s3bucketlogdestination-s3bucketarn)" : String
}
```

### YAML<a name="aws-properties-lex-botalias-s3bucketlogdestination-syntax.yaml"></a>

```
  [KmsKeyArn](#cfn-lex-botalias-s3bucketlogdestination-kmskeyarn): String
  [LogPrefix](#cfn-lex-botalias-s3bucketlogdestination-logprefix): String
  [S3BucketArn](#cfn-lex-botalias-s3bucketlogdestination-s3bucketarn): String
```

## Properties<a name="aws-properties-lex-botalias-s3bucketlogdestination-properties"></a>

`KmsKeyArn`  <a name="cfn-lex-botalias-s3bucketlogdestination-kmskeyarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Key Management Service \(KMS\) key for encrypting audio log files stored in an Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogPrefix`  <a name="cfn-lex-botalias-s3bucketlogdestination-logprefix"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketArn`  <a name="cfn-lex-botalias-s3bucketlogdestination-s3bucketarn"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)