# CloudFront DistributionConfig<a name="aws-properties-cloudfront-distributionconfig"></a>

`DistributionConfig` is a property of the AWS::CloudFront::Distribution property that describes which Amazon CloudFront origin servers to get your files from when users request the files through your website or application\.

## Syntax<a name="w3ab2c21c14d172b5"></a>

### JSON<a name="aws-properties-cloudfront-distributionconfig-syntax.json"></a>

```
{
   "Aliases" : [ String, ... ],
   "CacheBehaviors" : [ CacheBehavior, ... ],
   "Comment" : String,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-customerrorresponses)" : [ CustomErrorResponse, ... ],
   "DefaultCacheBehavior" : DefaultCacheBehavior,
   "DefaultRootObject" : String,
   "Enabled" : Boolean,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-httpversion)" : String,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distribution-distributionconfig-ipv6enabled)" : Boolean,
   "Logging" : Logging,
   "Origins" : [ Origin, ... ],
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-priceclass)" : String,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-restrictions)" : Restriction,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-viewercertificate)" : ViewerCertificate,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-webaclid)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distributionconfig-syntax.yaml"></a>

```
Aliases:
  - String
CacheBehaviors:
  CacheBehavior
Comment: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-customerrorresponses):
  CustomErrorResponse
DefaultCacheBehavior:
  DefaultCacheBehavior
DefaultRootObject: String
Enabled: Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-httpversion): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distribution-distributionconfig-ipv6enabled): Boolean
Logging:
  Logging
Origins:
  Origin
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-priceclass): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-restrictions):
  Restriction
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-viewercertificate):
  ViewerCertificate
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-webaclid): String
```

## Properties<a name="w3ab2c21c14d172b7"></a>

`Aliases`  
CNAMEs \(alternate domain names\), if any, for the distribution\.  
*Required: *No  
*Type*: List of String values

`CacheBehaviors`  
A list of CacheBehavior types for the distribution\.  
*Required: *No  
*Type*: List of CacheBehavior

`Comment`  
Any comments that you want to include about the distribution\. Optional\.  
When you create a distribution, you can include a comment of up to 128 characters\. You can update the comment at any time\.  
*Required: *No  
*Type*: String

`CustomErrorResponses`  
Whether CloudFront replaces HTTP status codes in the `4xx` and `5xx` range with custom error messages before returning the response to the viewer\.  
*Required: *No  
*Type* List of [CloudFront DistributionConfig CustomErrorResponse](aws-properties-cloudfront-distributionconfig-customerrorresponse.md)

`DefaultCacheBehavior`  
The default cache behavior that is triggered if you do not specify the `CacheBehavior` property or if files don't match any of the values of `PathPattern` in the `CacheBehavior` property\.  
*Required: *Yes  
*Type*: DefaultCacheBehavior type

`DefaultRootObject`  
The object \(such as `index.html`\) that you want CloudFront to request from your origin when the root URL for your distribution \(such as `http://example.com/`\) is requested\.  
Specifying a default root object avoids exposing the contents of your distribution\.
*Required: *No  
*Type*: String

`Enabled`  
Controls whether the distribution is enabled to accept end user requests for content\.  
*Required: *Yes  
*Type*: Boolean

`HttpVersion`  
The latest HTTP version that viewers can use to communicate with CloudFront\. Viewers that don't support the latest version automatically use an earlier HTTP version\. By default, AWS CloudFormation specifies `http1.1`\.  
For valid values, see the `HttpVersion` content for the [DistributionConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DistributionConfig.html) data type in the *Amazon CloudFront API Reference*\.  
*Required: *No  
*Type*: String

`IPV6Enabled`  
If you want CloudFront to respond to IPv6 DNS requests with an IPv6 address for your distribution, specify `true`\. If you specify `false`, CloudFront responds to IPv6 DNS requests with the DNS response code `NOERROR` and with no IP addresses\. This allows viewers to submit a second request, for an IPv4 address for your distribution\. For more information and usage guidance, see [CreateDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html#cloudfront-CreateDistribution-request-IsIPV6Enabled) in the *Amazon CloudFront API Reference*\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: No interruption 

`Logging`  
Controls whether access logs are written for the distribution\. To turn on access logs, specify this property\.  
*Required: *No  
*Type*: Logging type

`Origins`  
A list of origins for this CloudFront distribution\. For each origin, you can specify whether it is an Amazon S3 or custom origin\.  
*Required: *Yes  
*Type*: List of Origins\.

`PriceClass`  
The price class that corresponds with the maximum price that you want to pay for the CloudFront service\. For more information, see [Choosing the Price Class](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html) in the *Amazon CloudFront Developer Guide*\.  
For more information about the valid values, see the `PriceClass` content for the [DistributionConfig](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DistributionConfig.html) data type in the *Amazon CloudFront API Reference*\.  
*Required: *No  
*Type*: String

`Restrictions`  
Specifies restrictions on who or how viewers can access your content\.  
*Required: *No  
*Type*: [CloudFront DistributionConfiguration Restrictions](aws-properties-cloudfront-distributionconfig-restrictions.md)

`ViewerCertificate`  
The certificate to use when viewers use HTTPS to request objects\.  
*Required: *No  
*Type*: [CloudFront DistributionConfiguration ViewerCertificate](aws-properties-cloudfront-distributionconfig-viewercertificate.md)

`WebACLId`  
The AWS WAF web ACL to associate with this distribution\. AWS WAF is a web application firewall that enables you to monitor the HTTP and HTTPS requests that are forwarded to CloudFront and to control who can access your content\. CloudFront permits or forbids requests based on conditions that you specify, such as the IP addresses from which requests originate or the values of query strings\.  
*Required: *No  
*Type*: String