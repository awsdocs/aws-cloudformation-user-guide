# CloudFront Distribution Restrictions<a name="aws-properties-cloudfront-distribution-restrictions"></a>

`Restrictions` is a property of the [CloudFront Distribution DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md) property type that lets you limit which viewers can access your content\.

## Syntax<a name="w2922ab1c21c10c52c14c74b5"></a>

### JSON<a name="aws-properties-cloudfront-distribution-restrictions-syntax.json"></a>

```
{
  "[GeoRestriction](#cfn-cloudfront-distribution-restrictions-georestriction)" : GeoRestriction
}
```

### YAML<a name="aws-properties-cloudfront-distribution-restrictions-syntax.yaml"></a>

```
[GeoRestriction](#cfn-cloudfront-distribution-restrictions-georestriction): GeoRestriction
```

## Properties<a name="w2922ab1c21c10c52c14c74b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [Restrictions](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Restrictions.html) data type in the *Amazon CloudFront API Reference*\.

`GeoRestriction`  <a name="cfn-cloudfront-distribution-restrictions-georestriction"></a>
The countries in which viewers are able to access your content\.  
*Required*: Yes  
*Type*: [CloudFront Distribution GeoRestriction](aws-properties-cloudfront-distribution-georestriction.md)