# AWS::Glue::Crawler Targets<a name="aws-properties-glue-crawler-targets"></a>

Specifies data stores to crawl\.

## Syntax<a name="aws-properties-glue-crawler-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-targets-syntax.json"></a>

```
{
  "[CatalogTargets](#cfn-glue-crawler-targets-catalogtargets)" : [ CatalogTarget, ... ],
  "[DynamoDBTargets](#cfn-glue-crawler-targets-dynamodbtargets)" : [ DynamoDBTarget, ... ],
  "[JdbcTargets](#cfn-glue-crawler-targets-jdbctargets)" : [ JdbcTarget, ... ],
  "[S3Targets](#cfn-glue-crawler-targets-s3targets)" : [ S3Target, ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-targets-syntax.yaml"></a>

```
  [CatalogTargets](#cfn-glue-crawler-targets-catalogtargets): 
    - CatalogTarget
  [DynamoDBTargets](#cfn-glue-crawler-targets-dynamodbtargets): 
    - DynamoDBTarget
  [JdbcTargets](#cfn-glue-crawler-targets-jdbctargets): 
    - JdbcTarget
  [S3Targets](#cfn-glue-crawler-targets-s3targets): 
    - S3Target
```

## Properties<a name="aws-properties-glue-crawler-targets-properties"></a>

`CatalogTargets`  <a name="cfn-glue-crawler-targets-catalogtargets"></a>
Specifies AWS Glue Data Catalog targets\.  
*Required*: No  
*Type*: List of [CatalogTarget](aws-properties-glue-crawler-catalogtarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DynamoDBTargets`  <a name="cfn-glue-crawler-targets-dynamodbtargets"></a>
Specifies Amazon DynamoDB targets\.  
*Required*: No  
*Type*: List of [DynamoDBTarget](aws-properties-glue-crawler-dynamodbtarget.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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