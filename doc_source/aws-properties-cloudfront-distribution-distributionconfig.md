# AWS::CloudFront::Distribution DistributionConfig<a name="aws-properties-cloudfront-distribution-distributionconfig"></a>

A distribution configuration\.

## Syntax<a name="aws-properties-cloudfront-distribution-distributionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-distributionconfig-syntax.json"></a>

```
{
  "[Aliases](#cfn-cloudfront-distribution-distributionconfig-aliases)" : [ String, ... ],
  "[CacheBehaviors](#cfn-cloudfront-distribution-distributionconfig-cachebehaviors)" : [ CacheBehavior, ... ],
  "[Comment](#cfn-cloudfront-distribution-distributionconfig-comment)" : String,
  "[CustomErrorResponses](#cfn-cloudfront-distribution-distributionconfig-customerrorresponses)" : [ CustomErrorResponse, ... ],
  "[DefaultCacheBehavior](#cfn-cloudfront-distribution-distributionconfig-defaultcachebehavior)" : DefaultCacheBehavior,
  "[DefaultRootObject](#cfn-cloudfront-distribution-distributionconfig-defaultrootobject)" : String,
  "[Enabled](#cfn-cloudfront-distribution-distributionconfig-enabled)" : Boolean,
  "[HttpVersion](#cfn-cloudfront-distribution-distributionconfig-httpversion)" : String,
  "[IPV6Enabled](#cfn-cloudfront-distribution-distributionconfig-ipv6enabled)" : Boolean,
  "[Logging](#cfn-cloudfront-distribution-distributionconfig-logging)" : Logging,
  "[OriginGroups](#cfn-cloudfront-distribution-distributionconfig-origingroups)" : OriginGroups,
  "[Origins](#cfn-cloudfront-distribution-distributionconfig-origins)" : [ Origin, ... ],
  "[PriceClass](#cfn-cloudfront-distribution-distributionconfig-priceclass)" : String,
  "[Restrictions](#cfn-cloudfront-distribution-distributionconfig-restrictions)" : Restrictions,
  "[ViewerCertificate](#cfn-cloudfront-distribution-distributionconfig-viewercertificate)" : ViewerCertificate,
  "[WebACLId](#cfn-cloudfront-distribution-distributionconfig-webaclid)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-distributionconfig-syntax.yaml"></a>

```
  [Aliases](#cfn-cloudfront-distribution-distributionconfig-aliases): 
    - String
  [CacheBehaviors](#cfn-cloudfront-distribution-distributionconfig-cachebehaviors): 
    - CacheBehavior
  [Comment](#cfn-cloudfront-distribution-distributionconfig-comment): String
  [CustomErrorResponses](#cfn-cloudfront-distribution-distributionconfig-customerrorresponses): 
    - CustomErrorResponse
  [DefaultCacheBehavior](#cfn-cloudfront-distribution-distributionconfig-defaultcachebehavior): 
    DefaultCacheBehavior
  [DefaultRootObject](#cfn-cloudfront-distribution-distributionconfig-defaultrootobject): String
  [Enabled](#cfn-cloudfront-distribution-distributionconfig-enabled): Boolean
  [HttpVersion](#cfn-cloudfront-distribution-distributionconfig-httpversion): String
  [IPV6Enabled](#cfn-cloudfront-distribution-distributionconfig-ipv6enabled): Boolean
  [Logging](#cfn-cloudfront-distribution-distributionconfig-logging): 
    Logging
  [OriginGroups](#cfn-cloudfront-distribution-distributionconfig-origingroups): 
    OriginGroups
  [Origins](#cfn-cloudfront-distribution-distributionconfig-origins): 
    - Origin
  [PriceClass](#cfn-cloudfront-distribution-distributionconfig-priceclass): String
  [Restrictions](#cfn-cloudfront-distribution-distributionconfig-restrictions): 
    Restrictions
  [ViewerCertificate](#cfn-cloudfront-distribution-distributionconfig-viewercertificate): 
    ViewerCertificate
  [WebACLId](#cfn-cloudfront-distribution-distributionconfig-webaclid): String
```

## Properties<a name="aws-properties-cloudfront-distribution-distributionconfig-properties"></a>

`Aliases`  <a name="cfn-cloudfront-distribution-distributionconfig-aliases"></a>
A complex type that contains information about CNAMEs \(alternate domain names\), if any, for this distribution\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheBehaviors`  <a name="cfn-cloudfront-distribution-distributionconfig-cachebehaviors"></a>
A complex type that contains zero or more `CacheBehavior` elements\.   
*Required*: No  
*Type*: List of [CacheBehavior](aws-properties-cloudfront-distribution-cachebehavior.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comment`  <a name="cfn-cloudfront-distribution-distributionconfig-comment"></a>
Any comments you want to include about the distribution\.  
If you don't want to specify a comment, include an empty `Comment` element\.  
To delete an existing comment, update the distribution configuration and include an empty `Comment` element\.  
To add or change a comment, update the distribution configuration and specify the new comment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomErrorResponses`  <a name="cfn-cloudfront-distribution-distributionconfig-customerrorresponses"></a>
A complex type that controls the following:  
+ Whether CloudFront replaces HTTP status codes in the 4xx and 5xx range with custom error messages before returning the response to the viewer\.
+ How long CloudFront caches HTTP status codes in the 4xx and 5xx range\.
For more information about custom error pages, see [Customizing Error Responses](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/custom-error-pages.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of [CustomErrorResponse](aws-properties-cloudfront-distribution-customerrorresponse.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultCacheBehavior`  <a name="cfn-cloudfront-distribution-distributionconfig-defaultcachebehavior"></a>
A complex type that describes the default cache behavior if you don't specify a `CacheBehavior` element or if files don't match any of the values of `PathPattern` in `CacheBehavior` elements\. You must create exactly one default cache behavior\.  
*Required*: No  
*Type*: [DefaultCacheBehavior](aws-properties-cloudfront-distribution-defaultcachebehavior.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultRootObject`  <a name="cfn-cloudfront-distribution-distributionconfig-defaultrootobject"></a>
The object that you want CloudFront to request from your origin \(for example, `index.html`\) when a viewer requests the root URL for your distribution \(`http://www.example.com`\) instead of an object in your distribution \(`http://www.example.com/product-description.html`\)\. Specifying a default root object avoids exposing the contents of your distribution\.  
Specify only the object name, for example, `index.html`\. Don't add a `/` before the object name\.  
If you don't want to specify a default root object when you create a distribution, include an empty `DefaultRootObject` element\.  
To delete the default root object from an existing distribution, update the distribution configuration and include an empty `DefaultRootObject` element\.  
To replace the default root object, update the distribution configuration and specify the new object\.  
For more information about the default root object, see [Creating a Default Root Object](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DefaultRootObject.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-cloudfront-distribution-distributionconfig-enabled"></a>
From this field, you can enable or disable the selected distribution\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpVersion`  <a name="cfn-cloudfront-distribution-distributionconfig-httpversion"></a>
\(Optional\) Specify the maximum HTTP version that you want viewers to use to communicate with CloudFront\. The default value for new web distributions is `http1.1`\.  
For viewers and CloudFront to use HTTP/2, viewers must support TLS 1\.2 or later, and must support server name identification \(SNI\)\.  
In general, configuring CloudFront to communicate with viewers using HTTP/2 reduces latency\. You can improve performance by optimizing for HTTP/2\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http1.1 | http2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPV6Enabled`  <a name="cfn-cloudfront-distribution-distributionconfig-ipv6enabled"></a>
If you want CloudFront to respond to IPv6 DNS requests with an IPv6 address for your distribution, specify `true`\. If you specify `false`, CloudFront responds to IPv6 DNS requests with the DNS response code `NOERROR` and with no IP addresses\. This allows viewers to submit a second request, for an IPv4 address for your distribution\.   
In general, you should enable IPv6 if you have users on IPv6 networks who want to access your content\. However, if you're using signed URLs or signed cookies to restrict access to your content, and if you're using a custom policy that includes the `IpAddress` parameter to restrict the IP addresses that can access your content, don't enable IPv6\. If you want to restrict access to some content by IP address and not restrict access to other content \(or restrict access but not by IP address\), you can create two distributions\. For more information, see [Creating a Signed URL Using a Custom Policy](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-creating-signed-url-custom-policy.html) in the *Amazon CloudFront Developer Guide*\.  
If you're using an Amazon Route 53 alias resource record set to route traffic to your CloudFront distribution, you need to create a second alias resource record set when both of the following are true:  
+ You enable IPv6 for the distribution
+ You're using alternate domain names in the URLs for your objects
For more information, see [Routing Traffic to an Amazon CloudFront Web Distribution by Using Your Domain Name](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-cloudfront-distribution.html) in the *Amazon Route 53 Developer Guide*\.  
If you created a CNAME resource record set, either with Amazon Route 53 or with another DNS service, you don't need to make any changes\. A CNAME record will route traffic to your distribution regardless of the IP address format of the viewer request\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logging`  <a name="cfn-cloudfront-distribution-distributionconfig-logging"></a>
A complex type that controls whether access logs are written for the distribution\.  
For more information about logging, see [Access Logs](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/AccessLogs.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: [Logging](aws-properties-cloudfront-distribution-logging.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginGroups`  <a name="cfn-cloudfront-distribution-distributionconfig-origingroups"></a>
 A complex type that contains information about origin groups for this distribution\.  
*Required*: No  
*Type*: [OriginGroups](aws-properties-cloudfront-distribution-origingroups.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Origins`  <a name="cfn-cloudfront-distribution-distributionconfig-origins"></a>
A complex type that contains information about origins for this distribution\.   
*Required*: No  
*Type*: List of [Origin](aws-properties-cloudfront-distribution-origin.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PriceClass`  <a name="cfn-cloudfront-distribution-distributionconfig-priceclass"></a>
The price class that corresponds with the maximum price that you want to pay for CloudFront service\. If you specify `PriceClass_All`, CloudFront responds to requests for your objects from all CloudFront edge locations\.  
If you specify a price class other than `PriceClass_All`, CloudFront serves your objects from the CloudFront edge location that has the lowest latency among the edge locations in your price class\. Viewers who are in or near regions that are excluded from your specified price class may encounter slower performance\.  
For more information about price classes, see [Choosing the Price Class for a CloudFront Distribution](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html) in the *Amazon CloudFront Developer Guide*\. For information about CloudFront pricing, including how price classes \(such as Price Class 100\) map to CloudFront regions, see [Amazon CloudFront Pricing](http://aws.amazon.com/cloudfront/pricing/)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PriceClass_100 | PriceClass_200 | PriceClass_All`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Restrictions`  <a name="cfn-cloudfront-distribution-distributionconfig-restrictions"></a>
A complex type that identifies ways in which you want to restrict distribution of your content\.  
*Required*: No  
*Type*: [Restrictions](aws-properties-cloudfront-distribution-restrictions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ViewerCertificate`  <a name="cfn-cloudfront-distribution-distributionconfig-viewercertificate"></a>
A complex type that determines the distribution’s SSL/TLS configuration for communicating with viewers\.  
*Required*: No  
*Type*: [ViewerCertificate](aws-properties-cloudfront-distribution-viewercertificate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebACLId`  <a name="cfn-cloudfront-distribution-distributionconfig-webaclid"></a>
A unique identifier that specifies the AWS WAF web ACL, if any, to associate with this distribution\. To specify a web ACL created using the latest version of AWS WAF, use the ACL ARN, for example `arn:aws:wafv2:us-east-1:123456789012:global/webacl/ExampleWebACL/473e64fd-f30b-4765-81a0-62ad96dd167a`\. To specify a web ACL created using AWS WAF Classic, use the ACL ID, for example `473e64fd-f30b-4765-81a0-62ad96dd167a`\.  
AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to CloudFront, and lets you control access to your content\. Based on conditions that you specify, such as the IP addresses that requests originate from or the values of query strings, CloudFront responds to requests either with the requested content or with an HTTP 403 status code \(Forbidden\)\. You can also configure CloudFront to return a custom error page when a request is blocked\. For more information about AWS WAF, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-distributionconfig--seealso"></a>
+  [DistributionConfig](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DistributionConfig.html) in the *Amazon CloudFront API Reference* 

