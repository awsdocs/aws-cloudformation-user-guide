# AWS Glue Crawler S3Target<a name="aws-properties-glue-crawler-s3target"></a>

<a name="aws-properties-glue-crawler-s3target-description"></a>The `S3Target` property type specifies an Amazon S3 target for an AWS Glue crawl\.

<a name="aws-properties-glue-crawler-s3target-inheritance"></a> The `S3Targets` property of the [AWS Glue Crawler Targets](aws-properties-glue-crawler-targets.md) property type contains a list of `S3Target` property types\.

## Syntax<a name="aws-properties-glue-crawler-s3target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-s3target-syntax.json"></a>

```
{
  "[Path](#cfn-glue-crawler-s3target-path)" : String,
  "[Exclusions](#cfn-glue-crawler-s3target-exclusions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-s3target-syntax.yaml"></a>

```
[Path](#cfn-glue-crawler-s3target-path): String
[Exclusions](#cfn-glue-crawler-s3target-exclusions): 
  - String
```

## Properties<a name="aws-properties-glue-crawler-s3target-properties"></a>

For more information, see [S3Target Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-S3Target) in the *AWS Glue Developer Guide*\.

`Path`  <a name="cfn-glue-crawler-s3target-path"></a>
The path to the Amazon S3 target\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Exclusions`  <a name="cfn-glue-crawler-s3target-exclusions"></a>
A list of UTF\-8 strings that specify the Amazon S3 objects to exclude from the crawl\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 