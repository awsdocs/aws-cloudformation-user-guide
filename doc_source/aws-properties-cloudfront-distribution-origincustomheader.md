# AWS::CloudFront::Distribution OriginCustomHeader<a name="aws-properties-cloudfront-distribution-origincustomheader"></a>

A complex type that contains `HeaderName` and `HeaderValue` elements, if any, for this distribution\. 

## Syntax<a name="aws-properties-cloudfront-distribution-origincustomheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-origincustomheader-syntax.json"></a>

```
{
  "[HeaderName](#cfn-cloudfront-distribution-origincustomheader-headername)" : String,
  "[HeaderValue](#cfn-cloudfront-distribution-origincustomheader-headervalue)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origincustomheader-syntax.yaml"></a>

```
  [HeaderName](#cfn-cloudfront-distribution-origincustomheader-headername): String
  [HeaderValue](#cfn-cloudfront-distribution-origincustomheader-headervalue): String
```

## Properties<a name="aws-properties-cloudfront-distribution-origincustomheader-properties"></a>

`HeaderName`  <a name="cfn-cloudfront-distribution-origincustomheader-headername"></a>
The name of a header that you want CloudFront to forward to your origin\. For more information, see [Forwarding Custom Headers to Your Origin \(Web Distributions Only\)](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/forward-custom-headers.html) in the * Amazon CloudFront Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderValue`  <a name="cfn-cloudfront-distribution-origincustomheader-headervalue"></a>
The value for the header that you specified in the `HeaderName` field\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-cloudfront-distribution-origincustomheader--seealso"></a>
+  [OriginCustomHeader](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_OriginCustomHeader.html) in the *Amazon CloudFront API Reference* 

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
