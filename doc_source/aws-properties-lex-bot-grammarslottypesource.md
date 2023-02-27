# AWS::Lex::Bot GrammarSlotTypeSource<a name="aws-properties-lex-bot-grammarslottypesource"></a>

Describes the Amazon S3 bucket name and location for the grammar that is the source for the slot type\.

## Syntax<a name="aws-properties-lex-bot-grammarslottypesource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-grammarslottypesource-syntax.json"></a>

```
{
  "[KmsKeyArn](#cfn-lex-bot-grammarslottypesource-kmskeyarn)" : String,
  "[S3BucketName](#cfn-lex-bot-grammarslottypesource-s3bucketname)" : String,
  "[S3ObjectKey](#cfn-lex-bot-grammarslottypesource-s3objectkey)" : String
}
```

### YAML<a name="aws-properties-lex-bot-grammarslottypesource-syntax.yaml"></a>

```
  [KmsKeyArn](#cfn-lex-bot-grammarslottypesource-kmskeyarn): String
  [S3BucketName](#cfn-lex-bot-grammarslottypesource-s3bucketname): String
  [S3ObjectKey](#cfn-lex-bot-grammarslottypesource-s3objectkey): String
```

## Properties<a name="aws-properties-lex-bot-grammarslottypesource-properties"></a>

`KmsKeyArn`  <a name="cfn-lex-bot-grammarslottypesource-kmskeyarn"></a>
The AWS KMS key required to decrypt the contents of the grammar, if any\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3BucketName`  <a name="cfn-lex-bot-grammarslottypesource-s3bucketname"></a>
The name of the Amazon S3 bucket that contains the grammar source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ObjectKey`  <a name="cfn-lex-bot-grammarslottypesource-s3objectkey"></a>
The path to the grammar in the Amazon S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)