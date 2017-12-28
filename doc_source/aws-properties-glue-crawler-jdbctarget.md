# AWS Glue Crawler JdbcTarget<a name="aws-properties-glue-crawler-jdbctarget"></a>

<a name="aws-properties-glue-crawler-jdbctarget-description"></a>The `JdbcTarget` property type specifies a JDBC target for an AWS Glue crawl\.

<a name="aws-properties-glue-crawler-jdbctarget-inheritance"></a> The `JdbcTargets` property of the [AWS Glue Crawler Targets](aws-properties-glue-crawler-targets.md) property type contains a list of `JdbcTarget` property types\.

## Syntax<a name="aws-properties-glue-crawler-jdbctarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-jdbctarget-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-jdbctarget-connectionname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-jdbctarget-path)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-jdbctarget-exclusions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-jdbctarget-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-jdbctarget-connectionname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-jdbctarget-path): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-crawler-jdbctarget-exclusions): 
  - String
```

## Properties<a name="aws-properties-glue-crawler-jdbctarget-properties"></a>

For more information, see [JdbcTarget Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-JdbcTarget) in the *AWS Glue Developer Guide*\.

`ConnectionName`  
The name of the connection to use for the JDBC target\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Path`  
The path of the JDBC target\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Exclusions`  
A list of UTF\-8 strings that specify the items to exclude from the crawl\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: No interruption 