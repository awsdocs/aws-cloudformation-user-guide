# AWS::Route53::RecordSet GeoLocation<a name="aws-properties-route53-recordset-geolocation-1"></a>

A complex type that contains information about a geographic location\.

## Syntax<a name="aws-properties-route53-recordset-geolocation-1-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-recordset-geolocation-1-syntax.json"></a>

```
{
  "[ContinentCode](#cfn-route53-recordset-geolocation-continentcode)" : String,
  "[CountryCode](#cfn-route53-recordset-geolocation-countrycode)" : String,
  "[SubdivisionCode](#cfn-route53-recordset-geolocation-subdivisioncode)" : String
}
```

### YAML<a name="aws-properties-route53-recordset-geolocation-1-syntax.yaml"></a>

```
  [ContinentCode](#cfn-route53-recordset-geolocation-continentcode): String
  [CountryCode](#cfn-route53-recordset-geolocation-countrycode): String
  [SubdivisionCode](#cfn-route53-recordset-geolocation-subdivisioncode): String
```

## Properties<a name="aws-properties-route53-recordset-geolocation-1-properties"></a>

`ContinentCode`  <a name="cfn-route53-recordset-geolocation-continentcode"></a>
For geolocation resource record sets, a two\-letter abbreviation that identifies a continent\. Route 53 supports the following continent codes:  
+ **AF**: Africa
+ **AN**: Antarctica
+ **AS**: Asia
+ **EU**: Europe
+ **OC**: Oceania
+ **NA**: North America
+ **SA**: South America
Constraint: Specifying `ContinentCode` with either `CountryCode` or `SubdivisionCode` returns an `InvalidInput` error\.  
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CountryCode`  <a name="cfn-route53-recordset-geolocation-countrycode"></a>
For geolocation resource record sets, the two\-letter code for a country\.  
Route 53 uses the two\-letter country codes that are specified in [ISO standard 3166\-1 alpha\-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubdivisionCode`  <a name="cfn-route53-recordset-geolocation-subdivisioncode"></a>
For geolocation resource record sets, the two\-letter code for a state of the United States\. Route 53 doesn't support any other values for `SubdivisionCode`\. For a list of state abbreviations, see [Appendix B: Two–Letter State and Possession Abbreviations](https://pe.usps.com/text/pub28/28apb.htm) on the United States Postal Service website\.   
If you specify `subdivisioncode`, you must also specify `US` for `CountryCode`\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53-recordset-geolocation-1--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-recordset.html#aws-properties-route53-recordset-return-values) in the topic [AWS::Route53::RecordSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-recordset.html) 
+ [GeoLocation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_GeoLocation.html) in the *Amazon Route 53 API Reference*