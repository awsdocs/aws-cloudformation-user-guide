# CloudFront Distribution S3Origin<a name="aws-properties-cloudfront-distribution-s3originconfig"></a>

`S3Origin` is a property of the [Origin](aws-properties-cloudfront-distribution-origin.md) property that describes the Amazon Simple Storage Service \(S3\) origin to associate with an Amazon CloudFront origin\.

## Syntax<a name="w3ab2c21c14d303b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-s3originconfig-syntax.json"></a>

```
{
   "[OriginAccessIdentity](#cfn-cloudfront-distribution-s3originconfig-originaccessidentity)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-s3originconfig-syntax.yaml"></a>

```
[OriginAccessIdentity](#cfn-cloudfront-distribution-s3originconfig-originaccessidentity): String
```

## Properties<a name="w3ab2c21c14d303b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [S3Origin](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_S3Origin.html) data type in the *Amazon CloudFront API Reference*\.

`OriginAccessIdentity`  <a name="cfn-cloudfront-distribution-s3originconfig-originaccessidentity"></a>
The CloudFront origin access identity to associate with the origin\. You must specify the full origin ID—for example:  
`origin-access-identity/cloudfront/E15MNIMTCFKK4C`  
This is used to configure the origin so that end users can access objects in an Amazon S3 bucket through CloudFront only\.  
*Required*: No  
*Type*: String