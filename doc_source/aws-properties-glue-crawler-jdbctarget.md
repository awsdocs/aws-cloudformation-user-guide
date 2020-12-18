# AWS::Glue::Crawler JdbcTarget<a name="aws-properties-glue-crawler-jdbctarget"></a>

Specifies a JDBC data store to crawl\.

## Syntax<a name="aws-properties-glue-crawler-jdbctarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-jdbctarget-syntax.json"></a>

```
{
  "[ConnectionName](#cfn-glue-crawler-jdbctarget-connectionname)" : String,
  "[Exclusions](#cfn-glue-crawler-jdbctarget-exclusions)" : [ String, ... ],
  "[Path](#cfn-glue-crawler-jdbctarget-path)" : String
}
```

### YAML<a name="aws-properties-glue-crawler-jdbctarget-syntax.yaml"></a>

```
  [ConnectionName](#cfn-glue-crawler-jdbctarget-connectionname): String
  [Exclusions](#cfn-glue-crawler-jdbctarget-exclusions): 
    - String
  [Path](#cfn-glue-crawler-jdbctarget-path): String
```

## Properties<a name="aws-properties-glue-crawler-jdbctarget-properties"></a>

`ConnectionName`  <a name="cfn-glue-crawler-jdbctarget-connectionname"></a>
The name of the connection to use to connect to the JDBC target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Exclusions`  <a name="cfn-glue-crawler-jdbctarget-exclusions"></a>
A list of glob patterns used to exclude from the crawl\. For more information, see [Catalog Tables with a Crawler](https://docs.aws.amazon.com/glue/latest/dg/add-crawler.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-glue-crawler-jdbctarget-path"></a>
The path of the JDBC target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)