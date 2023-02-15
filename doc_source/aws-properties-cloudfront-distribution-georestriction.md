# AWS::CloudFront::Distribution GeoRestriction<a name="aws-properties-cloudfront-distribution-georestriction"></a>

A complex type that controls the countries in which your content is distributed\. CloudFront determines the location of your users using `MaxMind` GeoIP databases\. To disable geo restriction, remove the [Restrictions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-distributionconfig.html#cfn-cloudfront-distribution-distributionconfig-restrictions) property from your stack template\.

## Syntax<a name="aws-properties-cloudfront-distribution-georestriction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-georestriction-syntax.json"></a>

```
{
  "[Locations](#cfn-cloudfront-distribution-georestriction-locations)" : [ String, ... ],
  "[RestrictionType](#cfn-cloudfront-distribution-georestriction-restrictiontype)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-georestriction-syntax.yaml"></a>

```
  [Locations](#cfn-cloudfront-distribution-georestriction-locations): 
    - String
  [RestrictionType](#cfn-cloudfront-distribution-georestriction-restrictiontype): String
```

## Properties<a name="aws-properties-cloudfront-distribution-georestriction-properties"></a>

`Locations`  <a name="cfn-cloudfront-distribution-georestriction-locations"></a>
 A complex type that contains a `Location` element for each country in which you want CloudFront either to distribute your content \(`whitelist`\) or not distribute your content \(`blacklist`\)\.  
The `Location` element is a two\-letter, uppercase country code for a country that you want to include in your `blacklist` or `whitelist`\. Include one `Location` element for each country\.  
CloudFront and `MaxMind` both use `ISO 3166` country codes\. For the current list of countries and the corresponding codes, see `ISO 3166-1-alpha-2` code on the *International Organization for Standardization* website\. You can also refer to the country list on the CloudFront console, which includes both country names and codes\.  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestrictionType`  <a name="cfn-cloudfront-distribution-georestriction-restrictiontype"></a>
The method that you want to use to restrict distribution of your content by country:  
+  `none`: No geo restriction is enabled, meaning access to content is not restricted by client geo location\.
+  `blacklist`: The `Location` elements specify the countries in which you don't want CloudFront to distribute your content\.
+  `whitelist`: The `Location` elements specify the countries in which you want CloudFront to distribute your content\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `blacklist | none | whitelist`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-georestriction--seealso"></a>
+  [GeoRestriction](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_GeoRestriction.html) in the *Amazon CloudFront API Reference* 

