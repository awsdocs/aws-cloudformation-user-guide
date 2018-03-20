# CloudFront DistributionConfig Origin S3Origin<a name="aws-properties-cloudfront-s3origin"></a>

`S3Origin` is a property of the [Origin](aws-properties-cloudfront-origin.md) property that describes the Amazon Simple Storage Service \(S3\) origin to associate with an Amazon CloudFront origin\.

## Syntax<a name="w3ab2c21c14d215b5"></a>

### JSON<a name="aws-properties-cloudfront-s3origin-syntax.json"></a>

```
{
   "[OriginAccessIdentity](#cfn-cloudfront-s3origin-originaccessidentity)" : String
}
```

### YAML<a name="aws-properties-cloudfront-s3origin-syntax.yaml"></a>

```
[OriginAccessIdentity](#cfn-cloudfront-s3origin-originaccessidentity): String
```

## Properties<a name="w3ab2c21c14d215b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [S3Origin](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3Origin.html) data type in the *Amazon CloudFront API Reference*\.

`OriginAccessIdentity`  <a name="cfn-cloudfront-s3origin-originaccessidentity"></a>
The CloudFront origin access identity to associate with the origin\. You must specify the full origin ID—for example:  
`origin-access-identity/cloudfront/E15MNIMTCFKK4C`  
This is used to configure the origin so that end users can access objects in an Amazon S3 bucket through CloudFront only\.  
*Required: *No  
*Type*: String