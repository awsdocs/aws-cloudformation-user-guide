# AWS::CloudFront::Distribution DefaultCacheBehavior<a name="aws-properties-cloudfront-distribution-defaultcachebehavior"></a>

A complex type that describes the default cache behavior if you don’t specify a `CacheBehavior` element or if request URLs don’t match any of the values of `PathPattern` in `CacheBehavior` elements\. You must create exactly one default cache behavior\.

## Syntax<a name="aws-properties-cloudfront-distribution-defaultcachebehavior-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-defaultcachebehavior-syntax.json"></a>

```
{
  "[AllowedMethods](#cfn-cloudfront-distribution-defaultcachebehavior-allowedmethods)" : [ String, ... ],
  "[CachedMethods](#cfn-cloudfront-distribution-defaultcachebehavior-cachedmethods)" : [ String, ... ],
  "[CachePolicyId](#cfn-cloudfront-distribution-defaultcachebehavior-cachepolicyid)" : String,
  "[Compress](#cfn-cloudfront-distribution-defaultcachebehavior-compress)" : Boolean,
  "[DefaultTTL](#cfn-cloudfront-distribution-defaultcachebehavior-defaultttl)" : Double,
  "[FieldLevelEncryptionId](#cfn-cloudfront-distribution-defaultcachebehavior-fieldlevelencryptionid)" : String,
  "[ForwardedValues](#cfn-cloudfront-distribution-defaultcachebehavior-forwardedvalues)" : ForwardedValues,
  "[LambdaFunctionAssociations](#cfn-cloudfront-distribution-defaultcachebehavior-lambdafunctionassociations)" : [ LambdaFunctionAssociation, ... ],
  "[MaxTTL](#cfn-cloudfront-distribution-defaultcachebehavior-maxttl)" : Double,
  "[MinTTL](#cfn-cloudfront-distribution-defaultcachebehavior-minttl)" : Double,
  "[OriginRequestPolicyId](#cfn-cloudfront-distribution-defaultcachebehavior-originrequestpolicyid)" : String,
  "[RealtimeLogConfigArn](#cfn-cloudfront-distribution-defaultcachebehavior-realtimelogconfigarn)" : String,
  "[SmoothStreaming](#cfn-cloudfront-distribution-defaultcachebehavior-smoothstreaming)" : Boolean,
  "[TargetOriginId](#cfn-cloudfront-distribution-defaultcachebehavior-targetoriginid)" : String,
  "[TrustedKeyGroups](#cfn-cloudfront-distribution-defaultcachebehavior-trustedkeygroups)" : [ String, ... ],
  "[TrustedSigners](#cfn-cloudfront-distribution-defaultcachebehavior-trustedsigners)" : [ String, ... ],
  "[ViewerProtocolPolicy](#cfn-cloudfront-distribution-defaultcachebehavior-viewerprotocolpolicy)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-defaultcachebehavior-syntax.yaml"></a>

```
  [AllowedMethods](#cfn-cloudfront-distribution-defaultcachebehavior-allowedmethods): 
    - String
  [CachedMethods](#cfn-cloudfront-distribution-defaultcachebehavior-cachedmethods): 
    - String
  [CachePolicyId](#cfn-cloudfront-distribution-defaultcachebehavior-cachepolicyid): String
  [Compress](#cfn-cloudfront-distribution-defaultcachebehavior-compress): Boolean
  [DefaultTTL](#cfn-cloudfront-distribution-defaultcachebehavior-defaultttl): Double
  [FieldLevelEncryptionId](#cfn-cloudfront-distribution-defaultcachebehavior-fieldlevelencryptionid): String
  [ForwardedValues](#cfn-cloudfront-distribution-defaultcachebehavior-forwardedvalues): 
    ForwardedValues
  [LambdaFunctionAssociations](#cfn-cloudfront-distribution-defaultcachebehavior-lambdafunctionassociations): 
    - LambdaFunctionAssociation
  [MaxTTL](#cfn-cloudfront-distribution-defaultcachebehavior-maxttl): Double
  [MinTTL](#cfn-cloudfront-distribution-defaultcachebehavior-minttl): Double
  [OriginRequestPolicyId](#cfn-cloudfront-distribution-defaultcachebehavior-originrequestpolicyid): String
  [RealtimeLogConfigArn](#cfn-cloudfront-distribution-defaultcachebehavior-realtimelogconfigarn): String
  [SmoothStreaming](#cfn-cloudfront-distribution-defaultcachebehavior-smoothstreaming): Boolean
  [TargetOriginId](#cfn-cloudfront-distribution-defaultcachebehavior-targetoriginid): String
  [TrustedKeyGroups](#cfn-cloudfront-distribution-defaultcachebehavior-trustedkeygroups): 
    - String
  [TrustedSigners](#cfn-cloudfront-distribution-defaultcachebehavior-trustedsigners): 
    - String
  [ViewerProtocolPolicy](#cfn-cloudfront-distribution-defaultcachebehavior-viewerprotocolpolicy): String
```

## Properties<a name="aws-properties-cloudfront-distribution-defaultcachebehavior-properties"></a>

`AllowedMethods`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-allowedmethods"></a>
A complex type that controls which HTTP methods CloudFront processes and forwards to your Amazon S3 bucket or your custom origin\. There are three choices:  
+ CloudFront forwards only `GET` and `HEAD` requests\.
+ CloudFront forwards only `GET`, `HEAD`, and `OPTIONS` requests\.
+ CloudFront forwards `GET, HEAD, OPTIONS, PUT, PATCH, POST`, and `DELETE` requests\.
If you pick the third choice, you may need to restrict access to your Amazon S3 bucket or to your custom origin so users can't perform operations that you don't want them to\. For example, you might not want users to have permissions to delete objects from your origin\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CachedMethods`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-cachedmethods"></a>
A complex type that controls whether CloudFront caches the response to requests using the specified HTTP methods\. There are two choices:  
+ CloudFront caches responses to `GET` and `HEAD` requests\.
+ CloudFront caches responses to `GET`, `HEAD`, and `OPTIONS` requests\.
If you pick the second choice for your Amazon S3 Origin, you may need to forward Access\-Control\-Request\-Method, Access\-Control\-Request\-Headers, and Origin headers for the responses to be cached correctly\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CachePolicyId`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-cachepolicyid"></a>
The unique identifier of the cache policy that is attached to the default cache behavior\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) or [Using the managed cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-cache-policies.html) in the *Amazon CloudFront Developer Guide*\.  
A `DefaultCacheBehavior` must include either a `CachePolicyId` or `ForwardedValues`\. We recommend that you use a `CachePolicyId`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Compress`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-compress"></a>
Whether you want CloudFront to automatically compress certain files for this cache behavior\. If so, specify `true`; if not, specify `false`\. For more information, see [Serving Compressed Files](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/ServingCompressedFiles.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultTTL`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-defaultttl"></a>
This field is deprecated\. We recommend that you use the `DefaultTTL` field in a cache policy instead of this field\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) or [Using the managed cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-cache-policies.html) in the *Amazon CloudFront Developer Guide*\.  
The default amount of time that you want objects to stay in CloudFront caches before CloudFront forwards another request to your origin to determine whether the object has been updated\. The value that you specify applies only when your origin does not add HTTP headers such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\. For more information, see [Managing How Long Content Stays in an Edge Cache \(Expiration\)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Expiration.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldLevelEncryptionId`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-fieldlevelencryptionid"></a>
The value of `ID` for the field\-level encryption configuration that you want CloudFront to use for encrypting specific fields of data for the default cache behavior\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedValues`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-forwardedvalues"></a>
This field is deprecated\. We recommend that you use a cache policy or an origin request policy instead of this field\. For more information, see [Working with policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/working-with-policies.html) in the *Amazon CloudFront Developer Guide*\.  
If you want to include values in the cache key, use a cache policy\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) or [Using the managed cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-cache-policies.html) in the *Amazon CloudFront Developer Guide*\.  
If you want to send values to the origin but not include them in the cache key, use an origin request policy\. For more information, see [Creating origin request policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-origin-requests.html#origin-request-create-origin-request-policy) or [Using the managed origin request policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-origin-request-policies.html) in the *Amazon CloudFront Developer Guide*\.  
A `DefaultCacheBehavior` must include either a `CachePolicyId` or `ForwardedValues`\. We recommend that you use a `CachePolicyId`\.  
A complex type that specifies how CloudFront handles query strings, cookies, and HTTP headers\.  
*Required*: Conditional  
*Type*: [ForwardedValues](aws-properties-cloudfront-distribution-forwardedvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaFunctionAssociations`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-lambdafunctionassociations"></a>
A complex type that contains zero or more Lambda function associations for a cache behavior\.  
*Required*: No  
*Type*: List of [LambdaFunctionAssociation](aws-properties-cloudfront-distribution-lambdafunctionassociation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxTTL`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-maxttl"></a>
This field is deprecated\. We recommend that you use the `MaxTTL` field in a cache policy instead of this field\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) or [Using the managed cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-cache-policies.html) in the *Amazon CloudFront Developer Guide*\.  
The maximum amount of time that you want objects to stay in CloudFront caches before CloudFront forwards another request to your origin to determine whether the object has been updated\. The value that you specify applies only when your origin adds HTTP headers such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\. For more information, see [Managing How Long Content Stays in an Edge Cache \(Expiration\)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Expiration.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinTTL`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-minttl"></a>
This field is deprecated\. We recommend that you use the `MinTTL` field in a cache policy instead of this field\. For more information, see [Creating cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-key-create-cache-policy) or [Using the managed cache policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-cache-policies.html) in the *Amazon CloudFront Developer Guide*\.  
The minimum amount of time that you want objects to stay in CloudFront caches before CloudFront forwards another request to your origin to determine whether the object has been updated\. For more information, see [Managing How Long Content Stays in an Edge Cache \(Expiration\)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Expiration.html) in the *Amazon CloudFront Developer Guide*\.  
You must specify `0` for `MinTTL` if you configure CloudFront to forward all headers to your origin \(under `Headers`, if you specify `1` for `Quantity` and `*` for `Name`\)\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginRequestPolicyId`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-originrequestpolicyid"></a>
The unique identifier of the origin request policy that is attached to the default cache behavior\. For more information, see [Creating origin request policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-origin-requests.html#origin-request-create-origin-request-policy) or [Using the managed origin request policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-origin-request-policies.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RealtimeLogConfigArn`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-realtimelogconfigarn"></a>
The Amazon Resource Name \(ARN\) of the real\-time log configuration that is attached to this cache behavior\. For more information, see [Real\-time logs](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/real-time-logs.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SmoothStreaming`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-smoothstreaming"></a>
Indicates whether you want to distribute media files in the Microsoft Smooth Streaming format using the origin that is associated with this cache behavior\. If so, specify `true`; if not, specify `false`\. If you specify `true` for `SmoothStreaming`, you can still distribute other content using this cache behavior if the content matches the value of `PathPattern`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetOriginId`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-targetoriginid"></a>
The value of `ID` for the origin that you want CloudFront to route requests to when they use the default cache behavior\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustedKeyGroups`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-trustedkeygroups"></a>
A list of key groups that CloudFront can use to validate signed URLs or signed cookies\.  
When a cache behavior contains trusted key groups, CloudFront requires signed URLs or signed cookies for all requests that match the cache behavior\. The URLs or cookies must be signed with a private key whose corresponding public key is in the key group\. The signed URL or cookie contains information about which public key CloudFront should use to verify the signature\. For more information, see [Serving private content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustedSigners`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-trustedsigners"></a>
We recommend using `TrustedKeyGroups` instead of `TrustedSigners`\.
A list of AWS account IDs whose public keys CloudFront can use to validate signed URLs or signed cookies\.  
When a cache behavior contains trusted signers, CloudFront requires signed URLs or signed cookies for all requests that match the cache behavior\. The URLs or cookies must be signed with the private key of a CloudFront key pair in a trusted signer’s AWS account\. The signed URL or cookie contains information about which public key CloudFront should use to verify the signature\. For more information, see [Serving private content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ViewerProtocolPolicy`  <a name="cfn-cloudfront-distribution-defaultcachebehavior-viewerprotocolpolicy"></a>
The protocol that viewers can use to access the files in the origin specified by `TargetOriginId` when a request matches the path pattern in `PathPattern`\. You can specify the following options:  
+  `allow-all`: Viewers can use HTTP or HTTPS\.
+  `redirect-to-https`: If a viewer submits an HTTP request, CloudFront returns an HTTP status code of 301 \(Moved Permanently\) to the viewer along with the HTTPS URL\. The viewer then resubmits the request using the new URL\.
+  `https-only`: If a viewer sends an HTTP request, CloudFront returns an HTTP status code of 403 \(Forbidden\)\.
For more information about requiring the HTTPS protocol, see [Requiring HTTPS Between Viewers and CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https-viewers-to-cloudfront.html) in the *Amazon CloudFront Developer Guide*\.  
The only way to guarantee that viewers retrieve an object that was fetched from the origin using HTTPS is never to use any other protocol to fetch the object\. If you have recently changed from HTTP to HTTPS, we recommend that you clear your objects’ cache because cached objects are protocol agnostic\. That means that an edge location will return an object from the cache regardless of whether the current request protocol matches the protocol used previously\. For more information, see [Managing Cache Expiration](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Expiration.html) in the *Amazon CloudFront Developer Guide*\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `allow-all | https-only | redirect-to-https`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-defaultcachebehavior--seealso"></a>
+  [DefaultCacheBehavior](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_DefaultCacheBehavior.html) in the *Amazon CloudFront API Reference* 

