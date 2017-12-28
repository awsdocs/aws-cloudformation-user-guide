# CloudFront DefaultCacheBehavior<a name="aws-properties-cloudfront-defaultcachebehavior"></a>

`DefaultCacheBehavior` is a property of the DistributionConfig property that describes the default cache behavior for an Amazon CloudFront distribution\.

## Syntax<a name="w3ab2c21c14d186b5"></a>

### JSON<a name="aws-properties-cloudfront-defaultcachebehavior-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-allowedmethods)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-cachedmethods)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-compress)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-defaultttl)" : Number,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-forwardedvalues)" : ForwardedValues,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distribution-defaultcachebehavior-lambdafunctionassociations)" : [ LambdaFunctionAssociation, ... ]
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-maxttl)" : Number,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-minttl)" : Number,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-smoothstreaming)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-targetoriginid)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-trustedsigners)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-viewerprotocolpolicy)" : String
}
```

### YAML<a name="aws-properties-cloudfront-defaultcachebehavior-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-allowedmethods):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-cachedmethods):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-compress): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-defaultttl): Number
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-forwardedvalues):
  ForwardedValues
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distribution-defaultcachebehavior-lambdafunctionassociations): 
  - LambdaFunctionAssociation
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-maxttl): Number
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-minttl): Number
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-smoothstreaming): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-targetoriginid): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-trustedsigners):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-defaultcachebehavior-viewerprotocolpolicy) : String
```

## Properties<a name="w3ab2c21c14d186b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [DefaultCacheBehavior](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DefaultCacheBehavior.html) data type in the *Amazon CloudFront API Reference*\.

`AllowedMethods`  
HTTP methods that CloudFront processes and forwards to your Amazon S3 bucket or your custom origin\. In AWS CloudFormation templates, you can specify `["HEAD", "GET"]`, `["GET", "HEAD", "OPTIONS"]`, or `["DELETE", "GET", "HEAD", "OPTIONS", "PATCH", "POST", "PUT"]`\. If you don't specify a value, AWS CloudFormation specifies `["HEAD", "GET"]`\.  
*Required: *No  
*Type*: List of String values

`CachedMethods`  
HTTP methods for which CloudFront caches responses\. In AWS CloudFormation templates, you can specify `["HEAD", "GET"]` or `["GET", "HEAD", "OPTIONS"]`\. If you don't specify a value, AWS CloudFormation specifies `["HEAD", "GET"]`\.  
*Required: *No  
*Type*: List of String values

`Compress`  
Indicates whether CloudFront automatically compresses certain files for this cache behavior\. For more information, see [Serving Compressed Files](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/ServingCompressedFiles.html) in the *Amazon CloudFront Developer Guide*\.  
*Required: *No  
*Type*: Boolean

`DefaultTTL`  
The default time in seconds that objects stay in CloudFront caches before CloudFront forwards another request to your custom origin to determine whether the object has been updated\. This value applies only when your custom origin does not add HTTP headers, such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\.  
By default, AWS CloudFormation specifies `86400` seconds \(one day\)\. If the value of the `MinTTL` property is greater than the default value, CloudFront uses the minimum Time To Live \(TTL\) value\.  
*Required: *No  
*Type*: Number

`ForwardedValues`  
Specifies how CloudFront handles query strings or cookies\.  
*Required: *Yes  
*Type*: ForwardedValues type

`LambdaFunctionAssociations`  
Lambda function associations for the Amazon CloudFront distribution\.  
 *Required*: No  
 *Type*: List of [CloudFront Distribution LambdaFunctionAssociation](aws-properties-cloudfront-distribution-lambdafunctionassociation.md)  
 *Update requires*: No interruption 

`MaxTTL`  
The maximum time in seconds that objects stay in CloudFront caches before CloudFront forwards another request to your custom origin to determine whether the object has been updated\. This value applies only when your custom origin adds HTTP headers, such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\.  
By default, AWS CloudFormation specifies `31536000` seconds \(one year\)\. If the value of the `MinTTL` or `DefaultTTL` property is greater than the maximum value, CloudFront uses the default TTL value\.  
*Required: *No  
*Type*: Number

`MinTTL`  
The minimum amount of time that you want objects to stay in the cache before CloudFront queries your origin to see whether the object has been updated\.  
*Required: *No  
*Type*: Number

`SmoothStreaming`  
Indicates whether to use the origin that is associated with this cache behavior to distribute media files in the Microsoft Smooth Streaming format\.  
*Required: *No  
*Type*: Boolean

`TargetOriginId`  
The value of ID for the origin that CloudFront routes requests to when the default cache behavior is applied to a request\.  
*Required: *Yes  
*Type*: String

`TrustedSigners`  
A list of AWS accounts that can create signed URLs in order to access private content\.  
*Required: *No  
*Type*: List of String values

`ViewerProtocolPolicy`  
The protocol that users can use to access the files in the origin that you specified in the `TargetOriginId` property when the default cache behavior is applied to a request\. For more information about the valid values, see the `ViewerProtocolPolicy` content for the [DefaultCacheBehavior](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DefaultCacheBehavior.html) data type in the *Amazon CloudFront API Reference*\.  
*Required: *Yes  
*Type*: String