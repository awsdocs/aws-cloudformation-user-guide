# AWS::Kendra::DataSource WebCrawlerUrls<a name="aws-properties-kendra-datasource-webcrawlerurls"></a>

Specifies the seed or starting point URLs of the websites or the sitemap URLs of the websites you want to crawl\.

You can include website subdomains\. You can list up to 100 seed URLs and up to three sitemap URLs\.

You can only crawl websites that use the secure communication protocol, Hypertext Transfer Protocol Secure \(HTTPS\)\. If you receive an error when crawling a website, it could be that the website is blocked from crawling\.

 *When selecting websites to index, you must adhere to the [Amazon Acceptable Use Policy](http://aws.amazon.com/aup/) and all other Amazon terms\. Remember that you must only use the Amazon Kendra web crawler to index your own webpages, or webpages that you have authorization to index\.* 

## Syntax<a name="aws-properties-kendra-datasource-webcrawlerurls-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-webcrawlerurls-syntax.json"></a>

```
{
  "[SeedUrlConfiguration](#cfn-kendra-datasource-webcrawlerurls-seedurlconfiguration)" : WebCrawlerSeedUrlConfiguration,
  "[SiteMapsConfiguration](#cfn-kendra-datasource-webcrawlerurls-sitemapsconfiguration)" : WebCrawlerSiteMapsConfiguration
}
```

### YAML<a name="aws-properties-kendra-datasource-webcrawlerurls-syntax.yaml"></a>

```
  [SeedUrlConfiguration](#cfn-kendra-datasource-webcrawlerurls-seedurlconfiguration): 
    WebCrawlerSeedUrlConfiguration
  [SiteMapsConfiguration](#cfn-kendra-datasource-webcrawlerurls-sitemapsconfiguration): 
    WebCrawlerSiteMapsConfiguration
```

## Properties<a name="aws-properties-kendra-datasource-webcrawlerurls-properties"></a>

`SeedUrlConfiguration`  <a name="cfn-kendra-datasource-webcrawlerurls-seedurlconfiguration"></a>
Configuration of the seed or starting point URLs of the websites you want to crawl\.  
You can choose to crawl only the website host names, or the website host names with subdomains, or the website host names with subdomains and other domains that the webpages link to\.  
You can list up to 100 seed URLs\.  
*Required*: No  
*Type*: [WebCrawlerSeedUrlConfiguration](aws-properties-kendra-datasource-webcrawlerseedurlconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SiteMapsConfiguration`  <a name="cfn-kendra-datasource-webcrawlerurls-sitemapsconfiguration"></a>
Configuration of the sitemap URLs of the websites you want to crawl\.  
Only URLs belonging to the same website host names are crawled\. You can list up to three sitemap URLs\.  
*Required*: No  
*Type*: [WebCrawlerSiteMapsConfiguration](aws-properties-kendra-datasource-webcrawlersitemapsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)