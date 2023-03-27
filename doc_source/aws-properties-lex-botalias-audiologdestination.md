# AWS::Lex::BotAlias AudioLogDestination<a name="aws-properties-lex-botalias-audiologdestination"></a>

Specifies the S3 bucket location where audio logs are stored\.

## Syntax<a name="aws-properties-lex-botalias-audiologdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-botalias-audiologdestination-syntax.json"></a>

```
{
  "[S3Bucket](#cfn-lex-botalias-audiologdestination-s3bucket)" : S3BucketLogDestination
}
```

### YAML<a name="aws-properties-lex-botalias-audiologdestination-syntax.yaml"></a>

```
  [S3Bucket](#cfn-lex-botalias-audiologdestination-s3bucket): 
    S3BucketLogDestination
```

## Properties<a name="aws-properties-lex-botalias-audiologdestination-properties"></a>

`S3Bucket`  <a name="cfn-lex-botalias-audiologdestination-s3bucket"></a>
The S3 bucket location where audio logs are stored\.  
*Required*: Yes  
*Type*: [S3BucketLogDestination](aws-properties-lex-botalias-s3bucketlogdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)