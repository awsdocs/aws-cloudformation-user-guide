# AWS Glue Crawler Targets<a name="aws-properties-glue-crawler-targets"></a>

<a name="aws-properties-glue-crawler-targets-description"></a>The `Targets` property type specifies AWS Glue crawler targets\.

<a name="aws-properties-glue-crawler-targets-inheritance"></a> `Targets` is a property of the [AWS::Glue::Crawler](aws-resource-glue-crawler.md) resource\.

## Syntax<a name="aws-properties-glue-crawler-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-targets-syntax.json"></a>

```
{
  "[S3Targets](#cfn-glue-crawler-targets-s3targets)" : [ [*S3Target*](aws-properties-glue-crawler-s3target.md), ... ],
  "[JdbcTargets](#cfn-glue-crawler-targets-jdbctargets)" : [ [*JdbcTarget*](aws-properties-glue-crawler-jdbctarget.md), ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-targets-syntax.yaml"></a>

```
[S3Targets](#cfn-glue-crawler-targets-s3targets): 
  - [*S3Target*](aws-properties-glue-crawler-s3target.md)
[JdbcTargets](#cfn-glue-crawler-targets-jdbctargets): 
  - [*JdbcTarget*](aws-properties-glue-crawler-jdbctarget.md)
```

## Properties<a name="aws-properties-glue-crawler-targets-properties"></a>

For more information, see [CrawlerTargets Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-CrawlerTargets) in the *AWS Glue Developer Guide*\.

`S3Targets`  <a name="cfn-glue-crawler-targets-s3targets"></a>
The Amazon S3 crawler targets\.  
 *Required*: No  
 *Type*: List of [AWS Glue Crawler S3Target](aws-properties-glue-crawler-s3target.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`JdbcTargets`  <a name="cfn-glue-crawler-targets-jdbctargets"></a>
The JDBC crawler targets\.  
 *Required*: No  
 *Type*: List of [AWS Glue Crawler JdbcTarget](aws-properties-glue-crawler-jdbctarget.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 