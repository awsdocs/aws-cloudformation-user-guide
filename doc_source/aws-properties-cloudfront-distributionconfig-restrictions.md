# CloudFront DistributionConfiguration Restrictions<a name="aws-properties-cloudfront-distributionconfig-restrictions"></a>

`Restrictions` is a property of the [CloudFront DistributionConfig](aws-properties-cloudfront-distributionconfig.md) property that lets you limit which viewers can access your content\.

## Syntax<a name="w3ab2c21c14d218b5"></a>

### JSON<a name="aws-properties-cloudfront-distributionconfig-restrictions-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-restrictions-georestriction)" : GeoRestriction
}
```

### YAML<a name="aws-properties-cloudfront-distributionconfig-restrictions-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloudfront-distributionconfig-restrictions-georestriction): GeoRestriction
```

## Properties<a name="w3ab2c21c14d218b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [Restrictions](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Restrictions.html) data type in the *Amazon CloudFront API Reference*\.

`GeoRestriction`  
The countries in which viewers are able to access your content\.  
*Required: *Yes  
*Type*: [CloudFront DistributionConfig Restrictions GeoRestriction](aws-properties-cloudfront-distributionconfig-restrictions-georestriction.md)