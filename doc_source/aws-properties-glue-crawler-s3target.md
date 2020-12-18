# AWS::Glue::Crawler S3Target<a name="aws-properties-glue-crawler-s3target"></a>

Specifies a data store in Amazon Simple Storage Service \(Amazon S3\)\.

## Syntax<a name="aws-properties-glue-crawler-s3target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-s3target-syntax.json"></a>

```
{
  "[ConnectionName](#cfn-glue-crawler-s3target-connectionname)" : String,
  "[Exclusions](#cfn-glue-crawler-s3target-exclusions)" : [ String, ... ],
  "[Path](#cfn-glue-crawler-s3target-path)" : String
}
```

### YAML<a name="aws-properties-glue-crawler-s3target-syntax.yaml"></a>

```
  [ConnectionName](#cfn-glue-crawler-s3target-connectionname): String
  [Exclusions](#cfn-glue-crawler-s3target-exclusions): 
    - String
  [Path](#cfn-glue-crawler-s3target-path): String
```

## Properties<a name="aws-properties-glue-crawler-s3target-properties"></a>

`ConnectionName`  <a name="cfn-glue-crawler-s3target-connectionname"></a>
The name of a connection which allows a job or crawler to access data in Amazon S3 within an Amazon Virtual Private Cloud environment \(Amazon VPC\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Exclusions`  <a name="cfn-glue-crawler-s3target-exclusions"></a>
A list of glob patterns used to exclude from the crawl\. For more information, see [Catalog Tables with a Crawler](https://docs.aws.amazon.com/glue/latest/dg/add-crawler.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-glue-crawler-s3target-path"></a>
The path to the Amazon S3 target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)