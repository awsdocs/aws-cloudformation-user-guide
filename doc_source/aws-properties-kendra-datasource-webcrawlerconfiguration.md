# AWS::Kendra::DataSource WebCrawlerConfiguration<a name="aws-properties-kendra-datasource-webcrawlerconfiguration"></a>

<a name="aws-properties-kendra-datasource-webcrawlerconfiguration-description"></a>The `WebCrawlerConfiguration` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::Kendra::DataSource](aws-resource-kendra-datasource.md)\.

## Syntax<a name="aws-properties-kendra-datasource-webcrawlerconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-webcrawlerconfiguration-syntax.json"></a>

```
{
  "[AuthenticationConfiguration](#cfn-kendra-datasource-webcrawlerconfiguration-authenticationconfiguration)" : WebCrawlerAuthenticationConfiguration,
  "[CrawlDepth](#cfn-kendra-datasource-webcrawlerconfiguration-crawldepth)" : Integer,
  "[MaxContentSizePerPageInMegaBytes](#cfn-kendra-datasource-webcrawlerconfiguration-maxcontentsizeperpageinmegabytes)" : Double,
  "[MaxLinksPerPage](#cfn-kendra-datasource-webcrawlerconfiguration-maxlinksperpage)" : Integer,
  "[MaxUrlsPerMinuteCrawlRate](#cfn-kendra-datasource-webcrawlerconfiguration-maxurlsperminutecrawlrate)" : Integer,
  "[ProxyConfiguration](#cfn-kendra-datasource-webcrawlerconfiguration-proxyconfiguration)" : ProxyConfiguration,
  "[UrlExclusionPatterns](#cfn-kendra-datasource-webcrawlerconfiguration-urlexclusionpatterns)" : [ String, ... ],
  "[UrlInclusionPatterns](#cfn-kendra-datasource-webcrawlerconfiguration-urlinclusionpatterns)" : [ String, ... ],
  "[Urls](#cfn-kendra-datasource-webcrawlerconfiguration-urls)" : WebCrawlerUrls
}
```

### YAML<a name="aws-properties-kendra-datasource-webcrawlerconfiguration-syntax.yaml"></a>

```
  [AuthenticationConfiguration](#cfn-kendra-datasource-webcrawlerconfiguration-authenticationconfiguration): 
    WebCrawlerAuthenticationConfiguration
  [CrawlDepth](#cfn-kendra-datasource-webcrawlerconfiguration-crawldepth): Integer
  [MaxContentSizePerPageInMegaBytes](#cfn-kendra-datasource-webcrawlerconfiguration-maxcontentsizeperpageinmegabytes): Double
  [MaxLinksPerPage](#cfn-kendra-datasource-webcrawlerconfiguration-maxlinksperpage): Integer
  [MaxUrlsPerMinuteCrawlRate](#cfn-kendra-datasource-webcrawlerconfiguration-maxurlsperminutecrawlrate): Integer
  [ProxyConfiguration](#cfn-kendra-datasource-webcrawlerconfiguration-proxyconfiguration): 
    ProxyConfiguration
  [UrlExclusionPatterns](#cfn-kendra-datasource-webcrawlerconfiguration-urlexclusionpatterns): 
    - String
  [UrlInclusionPatterns](#cfn-kendra-datasource-webcrawlerconfiguration-urlinclusionpatterns): 
    - String
  [Urls](#cfn-kendra-datasource-webcrawlerconfiguration-urls): 
    WebCrawlerUrls
```

## Properties<a name="aws-properties-kendra-datasource-webcrawlerconfiguration-properties"></a>

`AuthenticationConfiguration`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-authenticationconfiguration"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [WebCrawlerAuthenticationConfiguration](aws-properties-kendra-datasource-webcrawlerauthenticationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrawlDepth`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-crawldepth"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxContentSizePerPageInMegaBytes`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-maxcontentsizeperpageinmegabytes"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxLinksPerPage`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-maxlinksperpage"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxUrlsPerMinuteCrawlRate`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-maxurlsperminutecrawlrate"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProxyConfiguration`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-proxyconfiguration"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [ProxyConfiguration](aws-properties-kendra-datasource-proxyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UrlExclusionPatterns`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-urlexclusionpatterns"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UrlInclusionPatterns`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-urlinclusionpatterns"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Urls`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-urls"></a>
Specifies the seed or starting point URLs of the websites or the sitemap URLs of the websites you want to crawl\.  
You can include website subdomains\. You can list up to 100 seed URLs and up to three sitemap URLs\.  
You can only crawl websites that use the secure communication protocol, Hypertext Transfer Protocol Secure \(HTTPS\)\. If you receive an error when crawling a website, it could be that the website is blocked from crawling\.  
 *When selecting websites to index, you must adhere to the [Amazon Acceptable Use Policy](http://aws.amazon.com/aup/) and all other Amazon terms\. Remember that you must only use the Amazon Kendra web crawler to index your own webpages, or webpages that you have authorization to index\.*   
*Required*: Yes  
*Type*: [WebCrawlerUrls](aws-properties-kendra-datasource-webcrawlerurls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)