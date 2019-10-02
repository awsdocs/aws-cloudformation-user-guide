# AWS::Route53::RecordSet GeoLocation<a name="aws-properties-route53-recordset-geolocation"></a>

A complex type that contains information about a geographic location\.

## Syntax<a name="aws-properties-route53-recordset-geolocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-recordset-geolocation-syntax.json"></a>

```
{
  "[ContinentCode](#cfn-route53-recordset-geolocation-continentcode)" : String,
  "[CountryCode](#cfn-route53-recordset-geolocation-countrycode)" : String,
  "[SubdivisionCode](#cfn-route53-recordset-geolocation-subdivisioncode)" : String
}
```

### YAML<a name="aws-properties-route53-recordset-geolocation-syntax.yaml"></a>

```
  [ContinentCode](#cfn-route53-recordset-geolocation-continentcode): String
  [CountryCode](#cfn-route53-recordset-geolocation-countrycode): String
  [SubdivisionCode](#cfn-route53-recordset-geolocation-subdivisioncode): String
```

## Properties<a name="aws-properties-route53-recordset-geolocation-properties"></a>

`ContinentCode`  <a name="cfn-route53-recordset-geolocation-continentcode"></a>
The two\-letter code for the continent\.  
Valid values: `AF` \| `AN` \| `AS` \| `EU` \| `OC` \| `NA` \| `SA`   
Constraint: Specifying `ContinentCode` with either `CountryCode` or `SubdivisionCode` returns an `InvalidInput` error\.  
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CountryCode`  <a name="cfn-route53-recordset-geolocation-countrycode"></a>
The two\-letter code for the country\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubdivisionCode`  <a name="cfn-route53-recordset-geolocation-subdivisioncode"></a>
The code for the subdivision\. Route 53 currently supports only states in the United States\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-route53-recordset-geolocation--seealso"></a>
+ [GeoLocation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_GeoLocation.html) in the *Amazon Route 53 API Reference*

## Supported Regions

This PropertyType is supported by ***all*** regions.