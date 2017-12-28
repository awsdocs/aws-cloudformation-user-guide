# CloudFront DistributionConfig Origin OriginCustomHeader<a name="aws-properties-cloudfront-origin-origincustomheader"></a>

`OriginCustomHeader` is a property of the Amazon CloudFront Origin property that specifies the custom headers CloudFront includes when it forwards requests to your origin\.

## Syntax<a name="w3ab2c21c14d209b5"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-origin-origincustomheader-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-origincustomheader-headername)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-origincustomheader-headervalue)" : String
}
```

### YAML<a name="aws-properties-cloudfront-origin-origincustomheader-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-origincustomheader-headername): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-origincustomheader-headervalue): String
```

## Properties<a name="w3ab2c21c14d209b7"></a>

`HeaderName`  
The name of a header that CloudFront forwards to your origin\. For more information, see [Forwarding Custom Headers to Your Origin \(Web Distributions Only\)](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/forward-custom-headers.html) in the *Amazon CloudFront Developer Guide*\.  
*Required: *Yes  
*Type*: String

`HeaderValue`  
The value for the header that you specified in the `HeaderName` property\.  
*Required: *Yes  
*Type*: String