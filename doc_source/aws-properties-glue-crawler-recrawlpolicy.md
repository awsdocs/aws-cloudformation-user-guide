# AWS::Glue::Crawler RecrawlPolicy<a name="aws-properties-glue-crawler-recrawlpolicy"></a>

When crawling an Amazon S3 data source after the first crawl is complete, specifies whether to crawl the entire dataset again or to crawl only folders that were added since the last crawler run\. For more information, see [Incremental Crawls in AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/incremental-crawls.html) in the developer guide\.

## Syntax<a name="aws-properties-glue-crawler-recrawlpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-recrawlpolicy-syntax.json"></a>

```
{
  "[RecrawlBehavior](#cfn-glue-crawler-recrawlpolicy-recrawlbehavior)" : String
}
```

### YAML<a name="aws-properties-glue-crawler-recrawlpolicy-syntax.yaml"></a>

```
  [RecrawlBehavior](#cfn-glue-crawler-recrawlpolicy-recrawlbehavior): String
```

## Properties<a name="aws-properties-glue-crawler-recrawlpolicy-properties"></a>

`RecrawlBehavior`  <a name="cfn-glue-crawler-recrawlpolicy-recrawlbehavior"></a>
Specifies whether to crawl the entire dataset again or to crawl only folders that were added since the last crawler run\.  
A value of `CRAWL_EVERYTHING` specifies crawling the entire dataset again\.  
A value of `CRAWL_NEW_FOLDERS_ONLY` specifies crawling only folders that were added since the last crawler run\.  
A value of `CRAWL_EVENT_MODE` specifies crawling only the changes identified by Amazon S3 events\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)