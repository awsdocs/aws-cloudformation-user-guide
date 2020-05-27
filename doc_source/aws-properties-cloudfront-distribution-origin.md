# AWS::CloudFront::Distribution Origin<a name="aws-properties-cloudfront-distribution-origin"></a>

A complex type that describes the Amazon S3 bucket, HTTP server \(for example, a web server\), Amazon MediaStore, or other server from which CloudFront gets your files\. This can also be an origin group, if you’ve created an origin group\. You must specify at least one origin or origin group\.

For the current quota \(limit\) on the number of origins or origin groups that you can specify for a distribution, see [Quotas](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cloudfront-limits.html) in the *Amazon CloudFront Developer Guide*\.

**Note**  
If you use CloudFormation to create a CloudFront distribution and an S3 bucket origin at the same time, the distribution might return `HTTP 307 Temporary Redirect` responses for up to 24 hours\. It can take up to 24 hours for the S3 bucket name to propagate to all AWS Regions\. When the propagation is complete, the CloudFront distribution will automatically stop sending these redirect responses; you don’t need to take any action\. For more information, see [Why am I getting an HTTP 307 Temporary Redirect response from Amazon S3?](http://aws.amazon.com/premiumsupport/knowledge-center/s3-http-307-response/) and [Temporary Request Redirection](https://docs.aws.amazon.com/AmazonS3/latest/dev/Redirects.html#TemporaryRedirection)\.

## Syntax<a name="aws-properties-cloudfront-distribution-origin-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-origin-syntax.json"></a>

```
{
  "[CustomOriginConfig](#cfn-cloudfront-distribution-origin-customoriginconfig)" : [CustomOriginConfig](aws-properties-cloudfront-distribution-customoriginconfig.md),
  "[DomainName](#cfn-cloudfront-distribution-origin-domainname)" : String,
  "[Id](#cfn-cloudfront-distribution-origin-id)" : String,
  "[OriginCustomHeaders](#cfn-cloudfront-distribution-origin-origincustomheaders)" : [ [OriginCustomHeader](aws-properties-cloudfront-distribution-origincustomheader.md), ... ],
  "[OriginPath](#cfn-cloudfront-distribution-origin-originpath)" : String,
  "[S3OriginConfig](#cfn-cloudfront-distribution-origin-s3originconfig)" : [S3OriginConfig](aws-properties-cloudfront-distribution-s3originconfig.md)
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origin-syntax.yaml"></a>

```
  [CustomOriginConfig](#cfn-cloudfront-distribution-origin-customoriginconfig): 
    [CustomOriginConfig](aws-properties-cloudfront-distribution-customoriginconfig.md)
  [DomainName](#cfn-cloudfront-distribution-origin-domainname): String
  [Id](#cfn-cloudfront-distribution-origin-id): String
  [OriginCustomHeaders](#cfn-cloudfront-distribution-origin-origincustomheaders): 
    - [OriginCustomHeader](aws-properties-cloudfront-distribution-origincustomheader.md)
  [OriginPath](#cfn-cloudfront-distribution-origin-originpath): String
  [S3OriginConfig](#cfn-cloudfront-distribution-origin-s3originconfig): 
    [S3OriginConfig](aws-properties-cloudfront-distribution-s3originconfig.md)
```

## Properties<a name="aws-properties-cloudfront-distribution-origin-properties"></a>

`CustomOriginConfig`  <a name="cfn-cloudfront-distribution-origin-customoriginconfig"></a>
Use this type to specify an origin that is a content container or HTTP server, including an Amazon S3 bucket that is configured with static website hosting\. To specify an Amazon S3 bucket that is * **not** * configured with static website hosting, use the `S3OriginConfig` type instead\.  
*Required*: Conditional  
*Type*: [CustomOriginConfig](aws-properties-cloudfront-distribution-customoriginconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-cloudfront-distribution-origin-domainname"></a>
The domain name for the origin\. For more information, see [Origin Domain Name](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesDomainName) in the *Amazon CloudFront Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-cloudfront-distribution-origin-id"></a>
A unique identifier for the origin\. This value must be unique within the distribution\.  
Use this value to specify the `TargetOriginId` in a CacheBehavior or [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-distributionconfig.html#cfn-cloudfront-distribution-distributionconfig-defaultcachebehavior)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginCustomHeaders`  <a name="cfn-cloudfront-distribution-origin-origincustomheaders"></a>
A list of HTTP header names and values that CloudFront adds to requests it sends to the origin\. For more information, see [Adding Custom Headers to Origin Requests](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/add-origin-custom-headers.html) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: List of [OriginCustomHeader](aws-properties-cloudfront-distribution-origincustomheader.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OriginPath`  <a name="cfn-cloudfront-distribution-origin-originpath"></a>
An optional path that CloudFront appends to the origin domain name when CloudFront requests content from the origin\. For more information, see [Origin Path](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesOriginPath) in the *Amazon CloudFront Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3OriginConfig`  <a name="cfn-cloudfront-distribution-origin-s3originconfig"></a>
Use this type to specify an origin that is an Amazon S3 bucket that is * **not** * configured with static website hosting\. To specify any other type of origin, including an Amazon S3 bucket that is configured with static website hosting, use the `CustomOriginConfig` type instead\.  
*Required*: Conditional  
*Type*: [S3OriginConfig](aws-properties-cloudfront-distribution-s3originconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-cloudfront-distribution-origin--seealso"></a>
+  [Origin](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Origin.html) in the *Amazon CloudFront API Reference* 