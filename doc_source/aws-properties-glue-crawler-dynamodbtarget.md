# AWS::Glue::Crawler DynamoDBTarget<a name="aws-properties-glue-crawler-dynamodbtarget"></a>

Specifies an Amazon DynamoDB table to crawl\.

## Syntax<a name="aws-properties-glue-crawler-dynamodbtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-dynamodbtarget-syntax.json"></a>

```
{
  "[Path](#cfn-glue-crawler-dynamodbtarget-path)" : String
}
```

### YAML<a name="aws-properties-glue-crawler-dynamodbtarget-syntax.yaml"></a>

```
  [Path](#cfn-glue-crawler-dynamodbtarget-path): String
```

## Properties<a name="aws-properties-glue-crawler-dynamodbtarget-properties"></a>

`Path`  <a name="cfn-glue-crawler-dynamodbtarget-path"></a>
The name of the DynamoDB table to crawl\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)