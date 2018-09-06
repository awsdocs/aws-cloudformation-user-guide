# CloudFront Distribution Origin<a name="aws-properties-cloudfront-distribution-origin"></a>

`Origin` is a property of the [DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md) property that describes an Amazon CloudFront distribution origin\.

## Syntax<a name="w3ab2c21c14d290b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-origin-syntax.json"></a>

```
{
  "[CustomOriginConfig](#cfn-cloudfront-distribution-origin-customorigin)" : CustomOriginConfig,
  "[DomainName](#cfn-cloudfront-distribution-origin-domainname)" : String,
  "[Id](#cfn-cloudfront-distribution-origin-id)" : String,
  "[OriginCustomHeaders](#cfn-cloudfront-distribution-origin-origincustomheaders)" : [ OriginCustomHeader, ... ]
  "[OriginPath](#cfn-cloudfront-distribution-origin-originpath)" : String,
  "[S3OriginConfig](#cfn-cloudfront-distribution-origin-s3origin)" : S3 Origin
}
```

### YAML<a name="aws-properties-cloudfront-distribution-origin-syntax.yaml"></a>

```
[CustomOriginConfig](#cfn-cloudfront-distribution-origin-customorigin):
  CustomOriginConfig
[DomainName](#cfn-cloudfront-distribution-origin-domainname): String
[Id](#cfn-cloudfront-distribution-origin-id): String
[OriginCustomHeaders](#cfn-cloudfront-distribution-origin-origincustomheaders):
  - OriginCustomHeader
[OriginPath](#cfn-cloudfront-distribution-origin-originpath): String
[S3OriginConfig](#cfn-cloudfront-distribution-origin-s3origin):
  S3 Origin
```

## Properties<a name="w3ab2c21c14d290b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [Origin](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Origin.html) data type in the *Amazon CloudFront API Reference*\.

`CustomOriginConfig`  <a name="cfn-cloudfront-distribution-origin-customorigin"></a>
Origin information to specify a custom origin\.  
*Required*: Conditional\. You cannot use `CustomOriginConfig` and `S3OriginConfig` in the same `Origin`, but you *must* specify one or the other\.  
*Type*: [CustomOriginConfig](aws-properties-cloudfront-distribution-customoriginconfig.md) type

`DomainName`  <a name="cfn-cloudfront-distribution-origin-domainname"></a>
The DNS name of the Amazon Simple Storage Service \(S3\) bucket or the HTTP server from which you want CloudFront to get objects for this origin\.  
*Required*: Yes  
*Type*: String

`Id`  <a name="cfn-cloudfront-distribution-origin-id"></a>
An identifier for the origin\. The value of `Id` must be unique within the distribution\.  
*Required*: Yes  
*Type*: String

`OriginCustomHeaders`  <a name="cfn-cloudfront-distribution-origin-origincustomheaders"></a>
Custom headers that CloudFront includes when it forwards a request to your origin\.  
*Required*: No  
*Type*: List of [OriginCustomHeader](aws-properties-cloudfront-distribution-origincustomheader.md) type

`OriginPath`  <a name="cfn-cloudfront-distribution-origin-originpath"></a>
The path that CloudFront uses to request content from an S3 bucket or custom origin\. The combination of the `DomainName` and `OriginPath` properties must resolve to a valid path\. The value must start with a slash mark \(`/`\) and cannot end with a slash mark\.  
*Required*: No  
*Type*: String

`S3OriginConfig`  <a name="cfn-cloudfront-distribution-origin-s3origin"></a>
Origin information to specify an S3 origin\.  
*Required*: Conditional\. You cannot use `S3OriginConfig` and `CustomOriginConfig` in the same `Origin`, but you *must* specify one or the other\.  
*Type*: [S3Origin](aws-properties-cloudfront-distribution-s3originconfig.md) type