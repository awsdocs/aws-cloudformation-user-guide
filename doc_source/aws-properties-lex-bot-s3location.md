# AWS::Lex::Bot S3Location<a name="aws-properties-lex-bot-s3location"></a>

Defines an Amazon S3 bucket location\. 

## Syntax<a name="aws-properties-lex-bot-s3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-s3location-syntax.json"></a>

```
{
  "[S3Bucket](#cfn-lex-bot-s3location-s3bucket)" : String,
  "[S3ObjectKey](#cfn-lex-bot-s3location-s3objectkey)" : String,
  "[S3ObjectVersion](#cfn-lex-bot-s3location-s3objectversion)" : String
}
```

### YAML<a name="aws-properties-lex-bot-s3location-syntax.yaml"></a>

```
  [S3Bucket](#cfn-lex-bot-s3location-s3bucket): String
  [S3ObjectKey](#cfn-lex-bot-s3location-s3objectkey): String
  [S3ObjectVersion](#cfn-lex-bot-s3location-s3objectversion): String
```

## Properties<a name="aws-properties-lex-bot-s3location-properties"></a>

`S3Bucket`  <a name="cfn-lex-bot-s3location-s3bucket"></a>
The S3 bucket name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ObjectKey`  <a name="cfn-lex-bot-s3location-s3objectkey"></a>
The path and file name to the object in the S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ObjectVersion`  <a name="cfn-lex-bot-s3location-s3objectversion"></a>
The version of the object in the S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)