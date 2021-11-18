# AWS::Kendra::DataSource WebCrawlerSeedUrlConfiguration<a name="aws-properties-kendra-datasource-webcrawlerseedurlconfiguration"></a>

Provides the configuration information of the seed or starting point URLs to crawl\.

 *When selecting websites to index, you must adhere to the [Amazon Acceptable Use Policy](http://aws.amazon.com/aup/) and all other Amazon terms\. Remember that you must only use the Amazon Kendra web crawler to index your own webpages, or webpages that you have authorization to index\.* 

## Syntax<a name="aws-properties-kendra-datasource-webcrawlerseedurlconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-webcrawlerseedurlconfiguration-syntax.json"></a>

```
{
  "[SeedUrls](#cfn-kendra-datasource-webcrawlerseedurlconfiguration-seedurls)" : [ String, ... ],
  "[WebCrawlerMode](#cfn-kendra-datasource-webcrawlerseedurlconfiguration-webcrawlermode)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-webcrawlerseedurlconfiguration-syntax.yaml"></a>

```
  [SeedUrls](#cfn-kendra-datasource-webcrawlerseedurlconfiguration-seedurls): 
    - String
  [WebCrawlerMode](#cfn-kendra-datasource-webcrawlerseedurlconfiguration-webcrawlermode): String
```

## Properties<a name="aws-properties-kendra-datasource-webcrawlerseedurlconfiguration-properties"></a>

`SeedUrls`  <a name="cfn-kendra-datasource-webcrawlerseedurlconfiguration-seedurls"></a>
The list of seed or starting point URLs of the websites you want to crawl\.  
The list can include a maximum of 100 seed URLs\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebCrawlerMode`  <a name="cfn-kendra-datasource-webcrawlerseedurlconfiguration-webcrawlermode"></a>
You can choose one of the following modes:  
+  `HOST_ONLY` – crawl only the website host names\. For example, if the seed URL is "abc\.example\.com", then only URLs with host name "abc\.example\.com" are crawled\.
+  `SUBDOMAINS` – crawl the website host names with subdomains\. For example, if the seed URL is "abc\.example\.com", then "a\.abc\.example\.com" and "b\.abc\.example\.com" are also crawled\.
+  `EVERYTHING` – crawl the website host names with subdomains and other domains that the webpages link to\.
The default mode is set to `HOST_ONLY`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EVERYTHING | HOST_ONLY | SUBDOMAINS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)