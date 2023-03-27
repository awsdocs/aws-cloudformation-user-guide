# AWS::Kendra::DataSource WebCrawlerConfiguration<a name="aws-properties-kendra-datasource-webcrawlerconfiguration"></a>

Provides the configuration information required for Amazon Kendra Web Crawler\.

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
Configuration information required to connect to websites using authentication\.  
You can connect to websites using basic authentication of user name and password\. You use a secret in [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) to store your authentication credentials\.  
You must provide the website host name and port number\. For example, the host name of https://a\.example\.com/page1\.html is "a\.example\.com" and the port is 443, the standard port for HTTPS\.  
*Required*: No  
*Type*: [WebCrawlerAuthenticationConfiguration](aws-properties-kendra-datasource-webcrawlerauthenticationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrawlDepth`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-crawldepth"></a>
Specifies the number of levels in a website that you want to crawl\.  
The first level begins from the website seed or starting point URL\. For example, if a website has 3 levels – index level \(i\.e\. seed in this example\), sections level, and subsections level – and you are only interested in crawling information up to the sections level \(i\.e\. levels 0\-1\), you can set your depth to 1\.  
The default crawl depth is set to 2\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxContentSizePerPageInMegaBytes`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-maxcontentsizeperpageinmegabytes"></a>
The maximum size \(in MB\) of a webpage or attachment to crawl\.  
Files larger than this size \(in MB\) are skipped/not crawled\.  
The default maximum size of a webpage or attachment is set to 50 MB\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxLinksPerPage`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-maxlinksperpage"></a>
The maximum number of URLs on a webpage to include when crawling a website\. This number is per webpage\.  
As a website’s webpages are crawled, any URLs the webpages link to are also crawled\. URLs on a webpage are crawled in order of appearance\.  
The default maximum links per page is 100\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxUrlsPerMinuteCrawlRate`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-maxurlsperminutecrawlrate"></a>
The maximum number of URLs crawled per website host per minute\.  
A minimum of one URL is required\.  
The default maximum number of URLs crawled per website host per minute is 300\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProxyConfiguration`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-proxyconfiguration"></a>
Configuration information required to connect to your internal websites via a web proxy\.  
You must provide the website host name and port number\. For example, the host name of https://a\.example\.com/page1\.html is "a\.example\.com" and the port is 443, the standard port for HTTPS\.  
Web proxy credentials are optional and you can use them to connect to a web proxy server that requires basic authentication\. To store web proxy credentials, you use a secret in [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)\.  
*Required*: No  
*Type*: [ProxyConfiguration](aws-properties-kendra-datasource-proxyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UrlExclusionPatterns`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-urlexclusionpatterns"></a>
A list of regular expression patterns to exclude certain URLs to crawl\. URLs that match the patterns are excluded from the index\. URLs that don't match the patterns are included in the index\. If a URL matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the URL file isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UrlInclusionPatterns`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-urlinclusionpatterns"></a>
A list of regular expression patterns to include certain URLs to crawl\. URLs that match the patterns are included in the index\. URLs that don't match the patterns are excluded from the index\. If a URL matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the URL file isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Urls`  <a name="cfn-kendra-datasource-webcrawlerconfiguration-urls"></a>
Specifies the seed or starting point URLs of the websites or the sitemap URLs of the websites you want to crawl\.  
You can include website subdomains\. You can list up to 100 seed URLs and up to three sitemap URLs\.  
You can only crawl websites that use the secure communication protocol, Hypertext Transfer Protocol Secure \(HTTPS\)\. If you receive an error when crawling a website, it could be that the website is blocked from crawling\.  
 *When selecting websites to index, you must adhere to the [Amazon Acceptable Use Policy](http://aws.amazon.com/aup/) and all other Amazon terms\. Remember that you must only use Amazon Kendra Web Crawler to index your own webpages, or webpages that you have authorization to index\.*   
*Required*: Yes  
*Type*: [WebCrawlerUrls](aws-properties-kendra-datasource-webcrawlerurls.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)