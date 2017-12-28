# AWS Glue Crawler Targets<a name="aws-properties-glue-crawler-targets"></a>

<a name="aws-properties-glue-crawler-targets-description"></a>The `Targets` property type specifies AWS Glue crawler targets\.

<a name="aws-properties-glue-crawler-targets-inheritance"></a> `Targets` is a property of the [AWS::Glue::Crawler](aws-resource-glue-crawler.md) resource\.

## Syntax<a name="aws-properties-glue-crawler-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-targets-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-targets-s3targets)" : [ S3Target, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-targets-jdbctargets)" : [ JdbcTarget, ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-targets-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-targets-s3targets): 
  - S3Target
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-targets-jdbctargets): 
  - JdbcTarget
```

## Properties<a name="aws-properties-glue-crawler-targets-properties"></a>

For more information, see [CrawlerTargets Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-CrawlerTargets) in the *AWS Glue Developer Guide*\.

`S3Targets`  
The Amazon S3 crawler targets\.  
 *Required*: No  
 *Type*: List of   
 *Update requires*: No interruption 

`JdbcTargets`  
The JDBC crawler targets\.  
 *Required*: No  
 *Type*: List of   
 *Update requires*: No interruption 