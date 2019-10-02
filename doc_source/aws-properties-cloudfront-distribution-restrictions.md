# AWS::CloudFront::Distribution Restrictions<a name="aws-properties-cloudfront-distribution-restrictions"></a>

A complex type that identifies ways in which you want to restrict distribution of your content\.

## Syntax<a name="aws-properties-cloudfront-distribution-restrictions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-restrictions-syntax.json"></a>

```
{
  "[GeoRestriction](#cfn-cloudfront-distribution-restrictions-georestriction)" : [GeoRestriction](aws-properties-cloudfront-distribution-georestriction.md)
}
```

### YAML<a name="aws-properties-cloudfront-distribution-restrictions-syntax.yaml"></a>

```
  [GeoRestriction](#cfn-cloudfront-distribution-restrictions-georestriction): 
    [GeoRestriction](aws-properties-cloudfront-distribution-georestriction.md)
```

## Properties<a name="aws-properties-cloudfront-distribution-restrictions-properties"></a>

`GeoRestriction`  <a name="cfn-cloudfront-distribution-restrictions-georestriction"></a>
A complex type that controls the countries in which your content is distributed\. CloudFront determines the location of your users using `MaxMind` GeoIP databases\.  
*Required*: Yes  
*Type*: [GeoRestriction](aws-properties-cloudfront-distribution-georestriction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-cloudfront-distribution-restrictions--seealso"></a>
+  [Restrictions](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Restrictions.html) in the *Amazon CloudFront API Reference* 

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
