# AWS::Lex::BotAlias S3BucketLogDestination<a name="aws-properties-lex-botalias-s3bucketlogdestination"></a>

Specifies an Amazon S3 bucket for logging audio conversations

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
The S3 prefix to assign to audio log files\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketArn`  <a name="cfn-lex-botalias-s3bucketlogdestination-s3bucketarn"></a>
The Amazon Resource Name \(ARN\) of an Amazon S3 bucket where audio log files are stored\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)