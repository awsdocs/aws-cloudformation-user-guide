# CloudFront Distribution CacheBehavior<a name="aws-properties-cloudfront-distribution-cachebehavior"></a>

`CacheBehavior` is a property of the [DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md) property that describes the Amazon CloudFront \(CloudFront\) cache behavior when the requested URL matches a pattern\.

## Syntax<a name="w3ab2c21c14d244b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-cachebehavior-syntax.json"></a>

```
{
  "[AllowedMethods](#cfn-cloudfront-distribution-cachebehavior-allowedmethods)" : [ String, ... ],
  "[CachedMethods](#cfn-cloudfront-distribution-cachebehavior-cachedmethods)" : [ String, ... ],
  "[Compress](#cfn-cloudfront-distribution-cachebehavior-compress)" : Boolean,
  "[DefaultTTL](#cfn-cloudfront-distribution-cachebehavior-defaultttl)" : Number,
  "[ForwardedValues](#cfn-cloudfront-distribution-cachebehavior-forwardedvalues)" : ForwardedValues,
  "[LambdaFunctionAssociations](#cfn-cloudfront-distribution-cachebehavior-lambdafunctionassociations)" : [ [*LambdaFunctionAssociation*](aws-properties-cloudfront-distribution-lambdafunctionassociation.md), ... ]
  "[MaxTTL](#cfn-cloudfront-distribution-cachebehavior-maxttl)" : Number,
  "[MinTTL](#cfn-cloudfront-distribution-cachebehavior-minttl)" : Number,
  "[PathPattern](#cfn-cloudfront-distribution-cachebehavior-pathpattern)" : String,
  "[SmoothStreaming](#cfn-cloudfront-distribution-cachebehavior-smoothstreaming)" : Boolean,
  "[TargetOriginId](#cfn-cloudfront-distribution-cachebehavior-targetoriginid)" : String,
  "[TrustedSigners](#cfn-cloudfront-distribution-cachebehavior-trustedsigners)" : [ String, ... ],
  "[ViewerProtocolPolicy](#cfn-cloudfront-distribution-cachebehavior-viewerprotocolpolicy)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-cachebehavior-syntax.yaml"></a>

```
[AllowedMethods](#cfn-cloudfront-distribution-cachebehavior-allowedmethods):
  - String
[CachedMethods](#cfn-cloudfront-distribution-cachebehavior-cachedmethods):
  - String
[Compress](#cfn-cloudfront-distribution-cachebehavior-compress): Boolean
[DefaultTTL](#cfn-cloudfront-distribution-cachebehavior-defaultttl): Number
[ForwardedValues](#cfn-cloudfront-distribution-cachebehavior-forwardedvalues):
  ForwardedValues
[LambdaFunctionAssociations](#cfn-cloudfront-distribution-cachebehavior-lambdafunctionassociations): 
  - [*LambdaFunctionAssociation*](aws-properties-cloudfront-distribution-lambdafunctionassociation.md)
[MaxTTL](#cfn-cloudfront-distribution-cachebehavior-maxttl): Number
[MinTTL](#cfn-cloudfront-distribution-cachebehavior-minttl): Number
[PathPattern](#cfn-cloudfront-distribution-cachebehavior-pathpattern): String
[SmoothStreaming](#cfn-cloudfront-distribution-cachebehavior-smoothstreaming): Boolean
[TargetOriginId](#cfn-cloudfront-distribution-cachebehavior-targetoriginid): String
[TrustedSigners](#cfn-cloudfront-distribution-cachebehavior-trustedsigners):
  - String
[ViewerProtocolPolicy](#cfn-cloudfront-distribution-cachebehavior-viewerprotocolpolicy): String
```

## Properties<a name="w3ab2c21c14d244b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [CacheBehavior](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CacheBehavior.html) data type in the *Amazon CloudFront API Reference*\.

`AllowedMethods`  <a name="cfn-cloudfront-distribution-cachebehavior-allowedmethods"></a>
HTTP methods that CloudFront processes and forwards to your Amazon S3 bucket or your custom origin\. You can specify `["HEAD", "GET"]`, `["GET", "HEAD", "OPTIONS"]`, or `["DELETE", "GET", "HEAD", "OPTIONS", "PATCH", "POST", "PUT"]`\. If you don't specify a value, AWS CloudFormation specifies `["HEAD", "GET"]`\.  
*Required*: No  
*Type*: List of String values

`CachedMethods`  <a name="cfn-cloudfront-distribution-cachebehavior-cachedmethods"></a>
HTTP methods for which CloudFront caches responses\. You can specify `["HEAD", "GET"]` or `["GET", "HEAD", "OPTIONS"]`\. If you don't specify a value, AWS CloudFormation specifies `["HEAD", "GET"]`\.  
*Required*: No  
*Type*: List of String values

`Compress`  <a name="cfn-cloudfront-distribution-cachebehavior-compress"></a>
Indicates whether CloudFront automatically compresses certain files for this cache behavior\. For more information, see [Serving Compressed Files](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/ServingCompressedFiles.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Boolean

`DefaultTTL`  <a name="cfn-cloudfront-distribution-cachebehavior-defaultttl"></a>
The default time in seconds that objects stay in CloudFront caches before CloudFront forwards another request to your custom origin to determine whether the object has been updated\. This value applies only when your custom origin does not add HTTP headers, such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\.  
By default, AWS CloudFormation specifies `86400` seconds \(one day\)\. If the value of the `MinTTL` property is greater than the default value, CloudFront uses the minimum Time to Live \(TTL\) value\.  
*Required*: No  
*Type*: Number

`ForwardedValues`  <a name="cfn-cloudfront-distribution-cachebehavior-forwardedvalues"></a>
Specifies how CloudFront handles query strings or cookies\.  
*Required*: Yes  
*Type*: [ForwardedValues](aws-properties-cloudfront-distribution-forwardedvalues.md) type

`LambdaFunctionAssociations`  <a name="cfn-cloudfront-distribution-cachebehavior-lambdafunctionassociations"></a>
Lambda function associations for the Amazon CloudFront distribution\.  
 *Required*: No  
 *Type*: List of [CloudFront Distribution LambdaFunctionAssociation](aws-properties-cloudfront-distribution-lambdafunctionassociation.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxTTL`  <a name="cfn-cloudfront-distribution-cachebehavior-maxttl"></a>
The maximum time in seconds that objects stay in CloudFront caches before CloudFront forwards another request to your custom origin to determine whether the object has been updated\. This value applies only when your custom origin does not add HTTP headers, such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\.  
By default, AWS CloudFormation specifies `31536000` seconds \(one year\)\. If the value of the `MinTTL` or `DefaultTTL` property is greater than the maximum value, CloudFront uses the default TTL value\.  
*Required*: No  
*Type*: Number

`MinTTL`  <a name="cfn-cloudfront-distribution-cachebehavior-minttl"></a>
The minimum amount of time that you want objects to stay in the cache before CloudFront queries your origin to see whether the object has been updated\.  
*Required*: No  
*Type*: Number

`PathPattern`  <a name="cfn-cloudfront-distribution-cachebehavior-pathpattern"></a>
The pattern to which this cache behavior applies\. For example, you can specify `images/*.jpg`\.  
When CloudFront receives an end\-user request, CloudFront compares the requested path with path patterns in the order in which cache behaviors are listed in the template\.  
*Required*: Yes  
*Type*: String

`SmoothStreaming`  <a name="cfn-cloudfront-distribution-cachebehavior-smoothstreaming"></a>
Indicates whether to use the origin that is associated with this cache behavior to distribute media files in the Microsoft Smooth Streaming format\. If you specify `true`, you can still use this cache behavior to distribute other content if the content matches the `PathPattern` value\.  
*Required*: No  
*Type*: Boolean

`TargetOriginId`  <a name="cfn-cloudfront-distribution-cachebehavior-targetoriginid"></a>
The ID value of the origin to which you want CloudFront to route requests when a request matches the value of the `PathPattern` property\.  
*Required*: Yes  
*Type*: String

`TrustedSigners`  <a name="cfn-cloudfront-distribution-cachebehavior-trustedsigners"></a>
A list of AWS accounts that can create signed URLs in order to access private content\.  
*Required*: No  
*Type*: List of String values

`ViewerProtocolPolicy`  <a name="cfn-cloudfront-distribution-cachebehavior-viewerprotocolpolicy"></a>
The protocol that users can use to access the files in the origin that you specified in the `TargetOriginId` property when a request matches the value of the `PathPattern` property\. For more information about the valid values, see the `ViewerProtocolPolicy` content for the [CacheBehavior](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CacheBehavior.html) data type in the *Amazon CloudFront API Reference*\.  
*Required*: Yes  
*Type*: String