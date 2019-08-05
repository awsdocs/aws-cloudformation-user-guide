# AWS::Glue::Crawler Targets<a name="aws-properties-glue-crawler-targets"></a>

Specifies data stores to crawl\.

## Syntax<a name="aws-properties-glue-crawler-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-targets-syntax.json"></a>

```
{
  "[JdbcTargets](#cfn-glue-crawler-targets-jdbctargets)" : [ [JdbcTarget](aws-properties-glue-crawler-jdbctarget.md), ... ],
  "[S3Targets](#cfn-glue-crawler-targets-s3targets)" : [ [S3Target](aws-properties-glue-crawler-s3target.md), ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-targets-syntax.yaml"></a>

```
  [JdbcTargets](#cfn-glue-crawler-targets-jdbctargets):
    - [JdbcTarget](aws-properties-glue-crawler-jdbctarget.md)
  [S3Targets](#cfn-glue-crawler-targets-s3targets):
    - [S3Target](aws-properties-glue-crawler-s3target.md)
```

## Properties<a name="aws-properties-glue-crawler-targets-properties"></a>

`JdbcTargets`  <a name="cfn-glue-crawler-targets-jdbctargets"></a>
Specifies JDBC targets\.
*Required*: No
*Type*: List of [JdbcTarget](aws-properties-glue-crawler-jdbctarget.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Targets`  <a name="cfn-glue-crawler-targets-s3targets"></a>
Specifies Amazon Simple Storage Service \(Amazon S3\) targets\.
*Required*: No
*Type*: List of [S3Target](aws-properties-glue-crawler-s3target.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
