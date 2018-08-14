# CloudFront Distribution DistributionConfig<a name="aws-properties-cloudfront-distribution-distributionconfig"></a>

`DistributionConfig` is a property of the [AWS::CloudFront::Distribution](aws-resource-cloudfront-distribution.md) property that describes which Amazon CloudFront origin servers to get your files from when users request the files through your website or application\.

## Syntax<a name="w3ab2c21c14d267b5"></a>

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
   "[Origins](#cfn-cloudfront-distribution-distributionconfig-origins)" : [ Origin, ... ],
   "[PriceClass](#cfn-cloudfront-distribution-distributionconfig-priceclass)" : String,
   "[Restrictions](#cfn-cloudfront-distribution-distributionconfig-restrictions)" : Restriction,
   "[ViewerCertificate](#cfn-cloudfront-distribution-distributionconfig-viewercertificate)" : ViewerCertificate,
   "[WebACLId](#cfn-cloudfront-distribution-distributionconfig-webaclid)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-distributionconfig-syntax.yaml"></a>

```
[Aliases](#cfn-cloudfront-distribution-distributionconfig-aliases):
  - String
[CacheBehaviors](#cfn-cloudfront-distribution-distributionconfig-cachebehaviors):
  CacheBehavior
[Comment](#cfn-cloudfront-distribution-distributionconfig-comment): String
[CustomErrorResponses](#cfn-cloudfront-distribution-distributionconfig-customerrorresponses):
  CustomErrorResponse
[DefaultCacheBehavior](#cfn-cloudfront-distribution-distributionconfig-defaultcachebehavior):
  DefaultCacheBehavior
[DefaultRootObject](#cfn-cloudfront-distribution-distributionconfig-defaultrootobject): String
[Enabled](#cfn-cloudfront-distribution-distributionconfig-enabled): Boolean
[HttpVersion](#cfn-cloudfront-distribution-distributionconfig-httpversion): String
[IPV6Enabled](#cfn-cloudfront-distribution-distributionconfig-ipv6enabled): Boolean
[Logging](#cfn-cloudfront-distribution-distributionconfig-logging):
  Logging
[Origins](#cfn-cloudfront-distribution-distributionconfig-origins):
  Origin
[PriceClass](#cfn-cloudfront-distribution-distributionconfig-priceclass): String
[Restrictions](#cfn-cloudfront-distribution-distributionconfig-restrictions):
  Restriction
[ViewerCertificate](#cfn-cloudfront-distribution-distributionconfig-viewercertificate):
  ViewerCertificate
[WebACLId](#cfn-cloudfront-distribution-distributionconfig-webaclid): String
```

## Properties<a name="w3ab2c21c14d267b7"></a>

`Aliases`  <a name="cfn-cloudfront-distribution-distributionconfig-aliases"></a>
CNAMEs \(alternate domain names\), if any, for the distribution\.  
*Required*: No  
*Type*: List of String values

`CacheBehaviors`  <a name="cfn-cloudfront-distribution-distributionconfig-cachebehaviors"></a>
A list of CacheBehavior types for the distribution\.  
*Required*: No  
*Type*: List of [CloudFront Distribution CacheBehavior](aws-properties-cloudfront-distribution-cachebehavior.md)

`Comment`  <a name="cfn-cloudfront-distribution-distributionconfig-comment"></a>
Any comments that you want to include about the distribution\. Optional\.  
When you create a distribution, you can include a comment of up to 128 characters\. You can update the comment at any time\.  
*Required*: No  
*Type*: String

`CustomErrorResponses`  <a name="cfn-cloudfront-distribution-distributionconfig-customerrorresponses"></a>
Whether CloudFront replaces HTTP status codes in the `4xx` and `5xx` range with custom error messages before returning the response to the viewer\.  
*Required*: No  
*Type* List of [CloudFront Distribution CustomErrorResponse](aws-properties-cloudfront-distribution-customerrorresponse.md)

`DefaultCacheBehavior`  <a name="cfn-cloudfront-distribution-distributionconfig-defaultcachebehavior"></a>
The default cache behavior that is triggered if you do not specify the `CacheBehavior` property or if files don't match any of the values of `PathPattern` in the `CacheBehavior` property\.  
*Required*: Yes  
*Type*: [DefaultCacheBehavior type](aws-properties-cloudfront-distribution-defaultcachebehavior.md)

`DefaultRootObject`  <a name="cfn-cloudfront-distribution-distributionconfig-defaultrootobject"></a>
The object \(such as `index.html`\) that you want CloudFront to request from your origin when the root URL for your distribution \(such as `http://example.com/`\) is requested\.  
Specifying a default root object avoids exposing the contents of your distribution\.
*Required*: No  
*Type*: String

`Enabled`  <a name="cfn-cloudfront-distribution-distributionconfig-enabled"></a>
Controls whether the distribution is enabled to accept end user requests for content\.  
*Required*: Yes  
*Type*: Boolean

`HttpVersion`  <a name="cfn-cloudfront-distribution-distributionconfig-httpversion"></a>
The latest HTTP version that viewers can use to communicate with CloudFront\. Viewers that don't support the latest version automatically use an earlier HTTP version\. By default, AWS CloudFormation specifies `http1.1`\.  
For valid values, see the `HttpVersion` content for the [DistributionConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DistributionConfig.html) data type in the *Amazon CloudFront API Reference*\.  
*Required*: No  
*Type*: String

`IPV6Enabled`  <a name="cfn-cloudfront-distribution-distributionconfig-ipv6enabled"></a>
If you want CloudFront to respond to IPv6 DNS requests with an IPv6 address for your distribution, specify `true`\. If you specify `false`, CloudFront responds to IPv6 DNS requests with the DNS response code `NOERROR` and with no IP addresses\. This allows viewers to submit a second request, for an IPv4 address for your distribution\. For more information and usage guidance, see [CreateDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html#cloudfront-CreateDistribution-request-IsIPV6Enabled) in the *Amazon CloudFront API Reference*\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Logging`  <a name="cfn-cloudfront-distribution-distributionconfig-logging"></a>
Controls whether access logs are written for the distribution\. To turn on access logs, specify this property\.  
*Required*: No  
*Type*: [Logging](aws-properties-cloudfront-distribution-logging.md) type

`Origins`  <a name="cfn-cloudfront-distribution-distributionconfig-origins"></a>
A list of origins for this CloudFront distribution\. For each origin, you can specify whether it is an Amazon S3 or custom origin\.  
*Required*: Yes  
*Type*: List of [Origins](aws-properties-cloudfront-distribution-origin.md)\.

`PriceClass`  <a name="cfn-cloudfront-distribution-distributionconfig-priceclass"></a>
The price class that corresponds with the maximum price that you want to pay for the CloudFront service\. For more information, see [Choosing the Price Class](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html) in the *Amazon CloudFront Developer Guide*\.  
For more information about the valid values, see the `PriceClass` content for the [DistributionConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DistributionConfig.html) data type in the *Amazon CloudFront API Reference*\.  
*Required*: No  
*Type*: String

`Restrictions`  <a name="cfn-cloudfront-distribution-distributionconfig-restrictions"></a>
Specifies restrictions on who or how viewers can access your content\.  
*Required*: No  
*Type*: [CloudFront Distribution Restrictions](aws-properties-cloudfront-distribution-restrictions.md)

`ViewerCertificate`  <a name="cfn-cloudfront-distribution-distributionconfig-viewercertificate"></a>
The certificate to use when viewers use HTTPS to request objects\.  
*Required*: No  
*Type*: [CloudFront Distribution ViewerCertificate](aws-properties-cloudfront-distribution-viewercertificate.md)

`WebACLId`  <a name="cfn-cloudfront-distribution-distributionconfig-webaclid"></a>
The AWS WAF [web ACL](aws-resource-waf-webacl.md) to associate with this distribution\. AWS WAF is a web application firewall that enables you to monitor the HTTP and HTTPS requests that are forwarded to CloudFront and to control who can access your content\. CloudFront permits or forbids requests based on conditions that you specify, such as the IP addresses from which requests originate or the values of query strings\.  
*Required*: No  
*Type*: String