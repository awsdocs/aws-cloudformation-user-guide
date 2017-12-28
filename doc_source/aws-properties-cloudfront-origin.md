# CloudFront DistributionConfig Origin<a name="aws-properties-cloudfront-origin"></a>

`Origin` is a property of the DistributionConfig property that describes an Amazon CloudFront distribution origin\.

## Syntax<a name="w3ab2c21c14d200b5"></a>

### JSON<a name="aws-properties-cloudfront-origin-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-customorigin)" : CustomOriginConfig,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-domainname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-origincustomheaders)" : [ OriginCustomHeader, ... ]
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-originpath)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-s3origin)" : S3 Origin
}
```

### YAML<a name="aws-properties-cloudfront-origin-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-customorigin):
  CustomOriginConfig
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-domainname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-origincustomheaders):
  - OriginCustomHeader
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-originpath): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-origin-s3origin):
  S3 Origin
```

## Properties<a name="w3ab2c21c14d200b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [Origin](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Origin.html) data type in the *Amazon CloudFront API Reference*\.

`CustomOriginConfig`  
Origin information to specify a custom origin\.  
*Required: *Conditional\. You cannot use `CustomOriginConfig` and `S3OriginConfig` in the same `Origin`, but you *must* specify one or the other\.  
*Type*: CustomOriginConfig type

`DomainName`  
The DNS name of the Amazon Simple Storage Service \(S3\) bucket or the HTTP server from which you want CloudFront to get objects for this origin\.  
*Required: *Yes  
*Type*: String

`Id`  
An identifier for the origin\. The value of `Id` must be unique within the distribution\.  
*Required: *Yes  
*Type*: String

`OriginCustomHeaders`  
Custom headers that CloudFront includes when it forwards a request to your origin\.  
*Required: *No  
*Type*: List of OriginCustomHeader type

`OriginPath`  
The path that CloudFront uses to request content from an S3 bucket or custom origin\. The combination of the `DomainName` and `OriginPath` properties must resolve to a valid path\. The value must start with a slash mark \(`/`\) and cannot end with a slash mark\.  
*Required: *No  
*Type*: String

`S3OriginConfig`  
Origin information to specify an S3 origin\.  
*Required: *Conditional\. You cannot use `S3OriginConfig` and `CustomOriginConfig` in the same `Origin`, but you *must* specify one or the other\.  
*Type*: S3Origin type