# CloudFront DistributionConfig Origin OriginCustomHeader<a name="aws-properties-cloudfront-origin-origincustomheader"></a>

`OriginCustomHeader` is a property of the [Amazon CloudFront Origin](aws-properties-cloudfront-origin.md) property that specifies the custom headers CloudFront includes when it forwards requests to your origin\.

## Syntax<a name="w3ab2c21c14d210b5"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-origin-origincustomheader-syntax.json"></a>

```
{
  "[HeaderName](#cfn-cloudfront-origin-origincustomheader-headername)" : String,
  "[HeaderValue](#cfn-cloudfront-origin-origincustomheader-headervalue)" : String
}
```

### YAML<a name="aws-properties-cloudfront-origin-origincustomheader-syntax.yaml"></a>

```
[HeaderName](#cfn-cloudfront-origin-origincustomheader-headername): String
[HeaderValue](#cfn-cloudfront-origin-origincustomheader-headervalue): String
```

## Properties<a name="w3ab2c21c14d210b7"></a>

`HeaderName`  <a name="cfn-cloudfront-origin-origincustomheader-headername"></a>
The name of a header that CloudFront forwards to your origin\. For more information, see [Forwarding Custom Headers to Your Origin \(Web Distributions Only\)](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/forward-custom-headers.html) in the *Amazon CloudFront Developer Guide*\.  
*Required: *Yes  
*Type*: String

`HeaderValue`  <a name="cfn-cloudfront-origin-origincustomheader-headervalue"></a>
The value for the header that you specified in the `HeaderName` property\.  
*Required: *Yes  
*Type*: String