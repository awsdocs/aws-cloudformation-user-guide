# AWS::CloudFront::OriginRequestPolicy OriginRequestPolicyConfig<a name="aws-properties-cloudfront-originrequestpolicy-originrequestpolicyconfig"></a>

An origin request policy configuration\.

This configuration determines the values that CloudFront includes in requests that it sends to the origin\. Each request that CloudFront sends to the origin includes the following:
+ The request body and the URL path \(without the domain name\) from the viewer request\.
+ The headers that CloudFront automatically includes in every origin request, including `Host`, `User-Agent`, and `X-Amz-Cf-Id`\.
+ All HTTP headers, cookies, and URL query strings that are specified in the cache policy or the origin request policy\. These can include items from the viewer request and, in the case of headers, additional ones that are added by CloudFront\.

CloudFront sends a request when it can’t find an object in its cache that matches the request\. If you want to send values to the origin and also include them in the cache key, use `CachePolicy`\.

## Syntax<a name="aws-properties-cloudfront-originrequestpolicy-originrequestpolicyconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-originrequestpolicy-originrequestpolicyconfig-syntax.json"></a>

```
{
  "[Comment](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-comment)" : String,
  "[CookiesConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-cookiesconfig)" : CookiesConfig,
  "[HeadersConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-headersconfig)" : HeadersConfig,
  "[Name](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-name)" : String,
  "[QueryStringsConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-querystringsconfig)" : QueryStringsConfig
}
```

### YAML<a name="aws-properties-cloudfront-originrequestpolicy-originrequestpolicyconfig-syntax.yaml"></a>

```
  [Comment](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-comment): String
  [CookiesConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-cookiesconfig): 
    CookiesConfig
  [HeadersConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-headersconfig): 
    HeadersConfig
  [Name](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-name): String
  [QueryStringsConfig](#cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-querystringsconfig): 
    QueryStringsConfig
```

## Properties<a name="aws-properties-cloudfront-originrequestpolicy-originrequestpolicyconfig-properties"></a>

`Comment`  <a name="cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-comment"></a>
A comment to describe the origin request policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CookiesConfig`  <a name="cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-cookiesconfig"></a>
The cookies from viewer requests to include in origin requests\.  
*Required*: Yes  
*Type*: [CookiesConfig](aws-properties-cloudfront-originrequestpolicy-cookiesconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeadersConfig`  <a name="cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-headersconfig"></a>
The HTTP headers to include in origin requests\. These can include headers from viewer requests and additional headers added by CloudFront\.  
*Required*: Yes  
*Type*: [HeadersConfig](aws-properties-cloudfront-originrequestpolicy-headersconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-name"></a>
A unique name to identify the origin request policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringsConfig`  <a name="cfn-cloudfront-originrequestpolicy-originrequestpolicyconfig-querystringsconfig"></a>
The URL query strings from viewer requests to include in origin requests\.  
*Required*: Yes  
*Type*: [QueryStringsConfig](aws-properties-cloudfront-originrequestpolicy-querystringsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)