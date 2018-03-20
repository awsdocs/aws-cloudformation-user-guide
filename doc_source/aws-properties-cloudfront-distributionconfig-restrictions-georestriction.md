# CloudFront DistributionConfig Restrictions GeoRestriction<a name="aws-properties-cloudfront-distributionconfig-restrictions-georestriction"></a>

`GeoRestriction` is a property of the [CloudFront DistributionConfiguration Restrictions](aws-properties-cloudfront-distributionconfig-restrictions.md) property that describes the countries in which Amazon CloudFront allows viewers to access your content\.

## Syntax<a name="w3ab2c21c14d223b5"></a>

### JSON<a name="aws-properties-cloudfront-distributionconfig-restrictions-georestriction-syntax.json"></a>

```
{
  "[Locations](#cfn-cloudfront-distributionconfig-restrictions-georestriction-locations)" : [ String, ... ],
  "[RestrictionType](#cfn-cloudfront-distributionconfig-restrictions-georestriction-restrictiontype)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distributionconfig-restrictions-georestriction-syntax.yaml"></a>

```
[Locations](#cfn-cloudfront-distributionconfig-restrictions-georestriction-locations):
  - String
[RestrictionType](#cfn-cloudfront-distributionconfig-restrictions-georestriction-restrictiontype): String
```

## Properties<a name="w3ab2c21c14d223b7"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [GeoRestriction](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_GeoRestriction.html) data type in the *Amazon CloudFront API Reference*\.

`Locations`  <a name="cfn-cloudfront-distributionconfig-restrictions-georestriction-locations"></a>
The two\-letter, uppercase country code for a country that you want to include in your blacklist or whitelist\.  
*Required: *Conditional\. Required if you specified `blacklist` or `whitelist` for the `RestrictionType` property\.  
*Type*: List of String values

`RestrictionType`  <a name="cfn-cloudfront-distributionconfig-restrictions-georestriction-restrictiontype"></a>
The method to restrict distribution of your content:    
`blacklist`  
Prevents viewers in the countries that you specified from accessing your content\.  
`whitelist`  
Allows viewers in the countries that you specified to access your content\.  
`none`  
No distribution restrictions by country\.
*Required: *Yes  
*Type*: String