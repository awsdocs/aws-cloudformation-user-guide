# AWS::CloudFront::Distribution Origin<a name="aws-properties-cloudfront-distribution-origin"></a>

An origin\.

An origin is the location where content is stored, and from which CloudFront gets content to serve to viewers\. To specify an origin:
+ Use `S3OriginConfig` to specify an Amazon S3 bucket that is not configured with static website hosting\.
+ Use `CustomOriginConfig` to specify all other kinds of origins, including:
  + An Amazon S3 bucket that is configured with static website hosting
  + An Elastic Load Balancing load balancer
  + An AWS Elemental MediaPackage endpoint
  + An AWS Elemental MediaStore container
  + Any other HTTP server, running on an Amazon EC2 instance or any other kind of host

For the current maximum number of origins that you can specify per distribution, see [General Quotas on Web Distributions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cloudfront-limits.html#limits-web-distributions) in the *Amazon CloudFront Developer Guide* \(quotas were formerly referred to as limits\)\.

## Syntax<a name="aws-properties-cloudfront-distribution-origin-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-origin-syntax.json"></a>

```
{
  "[ConnectionAttempts](#cfn-cloudfront-distribution-origin-connectionattempts)" : Integer,
  "[ConnectionTimeout](#cfn-cloudfront-distribution-origin-connectiontimeout)" : Integer,
  "[CustomOriginConfig](#cfn-cloudfront-distribution-origin-customoriginconfig)" : CustomOriginConfig,
  "[DomainName](#cfn-cloudfront-distribution-origin-domainname)" : String,
  "[Id](#cfn-cloudfront-distribution-origin-id)" : String,
  "[OriginCustomHeaders](#cfn-cloudfront-distribution-origin-origincustomheaders)" : [ OriginCustomHeader, ... ],
  "[OriginPath](#cfn-cloudfront-distribution-origin-originpath)" : String,
  "[OriginShield](#cfn-cloudfront-distribution-origin-originshield)" : OriginShield,
  "[S3OriginConfig](#cfn-cloudfront-distribution-origin-s3originconfig)" : S3OriginConfig
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origin-syntax.yaml"></a>

```
  [ConnectionAttempts](#cfn-cloudfront-distribution-origin-connectionattempts): Integer
  [ConnectionTimeout](#cfn-cloudfront-distribution-origin-connectiontimeout): Integer
  [CustomOriginConfig](#cfn-cloudfront-distribution-origin-customoriginconfig): 
    CustomOriginConfig
  [DomainName](#cfn-cloudfront-distribution-origin-domainname): String
  [Id](#cfn-cloudfront-distribution-origin-id): String
  [OriginCustomHeaders](#cfn-cloudfront-distribution-origin-origincustomheaders): 
    - OriginCustomHeader
  [OriginPath](#cfn-cloudfront-distribution-origin-originpath): String
  [OriginShield](#cfn-cloudfront-distribution-origin-originshield): 
    OriginShield
  [S3OriginConfig](#cfn-cloudfront-distribution-origin-s3originconfig): 
    S3OriginConfig
```

## Properties<a name="aws-properties-cloudfront-distribution-origin-properties"></a>

`ConnectionAttempts`  <a name="cfn-cloudfront-distribution-origin-connectionattempts"></a>
The number of times that CloudFront attempts to connect to the origin\. The minimum number is 1, the maximum is 3, and the default \(if you don’t specify otherwise\) is 3\.  
For a custom origin \(including an Amazon S3 bucket that’s configured with static website hosting\), this value also specifies the number of times that CloudFront attempts to get a response from the origin, in the case of an [Origin Response Timeout](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesOriginResponseTimeout)\.  
For more information, see [Origin Connection Attempts](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#origin-connection-attempts) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionTimeout`  <a name="cfn-cloudfront-distribution-origin-connectiontimeout"></a>
The number of seconds that CloudFront waits when trying to establish a connection to the origin\. The minimum timeout is 1 second, the maximum is 10 seconds, and the default \(if you don’t specify otherwise\) is 10 seconds\.  
For more information, see [Origin Connection Timeout](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#origin-connection-timeout) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomOriginConfig`  <a name="cfn-cloudfront-distribution-origin-customoriginconfig"></a>
Use this type to specify an origin that is not an Amazon S3 bucket, with one exception\. If the Amazon S3 bucket is configured with static website hosting, use this type\. If the Amazon S3 bucket is not configured with static website hosting, use the `S3OriginConfig` type instead\.  
*Required*: Conditional  
*Type*: [CustomOriginConfig](aws-properties-cloudfront-distribution-customoriginconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-cloudfront-distribution-origin-domainname"></a>
The domain name for the origin\.  
For more information, see [Origin Domain Name](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesDomainName) in the *Amazon CloudFront Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-cloudfront-distribution-origin-id"></a>
A unique identifier for the origin\. This value must be unique within the distribution\.  
Use this value to specify the `TargetOriginId` in a `CacheBehavior` or `DefaultCacheBehavior`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginCustomHeaders`  <a name="cfn-cloudfront-distribution-origin-origincustomheaders"></a>
A list of HTTP header names and values that CloudFront adds to the requests that it sends to the origin\.  
For more information, see [Adding Custom Headers to Origin Requests](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/add-origin-custom-headers.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of [OriginCustomHeader](aws-properties-cloudfront-distribution-origincustomheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginPath`  <a name="cfn-cloudfront-distribution-origin-originpath"></a>
An optional path that CloudFront appends to the origin domain name when CloudFront requests content from the origin\.  
For more information, see [Origin Path](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesOriginPath) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginShield`  <a name="cfn-cloudfront-distribution-origin-originshield"></a>
CloudFront Origin Shield\. Using Origin Shield can help reduce the load on your origin\.  
For more information, see [Using Origin Shield](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/origin-shield.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: [OriginShield](aws-properties-cloudfront-distribution-originshield.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3OriginConfig`  <a name="cfn-cloudfront-distribution-origin-s3originconfig"></a>
Use this type to specify an origin that is an Amazon S3 bucket that is not configured with static website hosting\. To specify any other type of origin, including an Amazon S3 bucket that is configured with static website hosting, use the `CustomOriginConfig` type instead\.  
*Required*: Conditional  
*Type*: [S3OriginConfig](aws-properties-cloudfront-distribution-s3originconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-origin--seealso"></a>
+  [Origin](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Origin.html) in the *Amazon CloudFront API Reference* 

