# AWS::Location::PlaceIndex<a name="aws-resource-location-placeindex"></a>

Specifies a place index resource in your AWS account\. Use a place index resource to geocode addresses and other text queries by using the `SearchPlaceIndexForText` operation, and reverse geocode coordinates by using the `SearchPlaceIndexForPosition` operation, and enable autosuggestions by using the `SearchPlaceIndexForSuggestions` operation\.

**Note**  
If your application is tracking or routing assets you use in your business, such as delivery vehicles or employees, you must not use Esri as your geolocation provider\. See section 82 of the [AWS service terms](http://aws.amazon.com/service-terms) for more details\.

## Syntax<a name="aws-resource-location-placeindex-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-location-placeindex-syntax.json"></a>

```
{
  "Type" : "AWS::Location::PlaceIndex",
  "Properties" : {
      "[DataSource](#cfn-location-placeindex-datasource)" : String,
      "[DataSourceConfiguration](#cfn-location-placeindex-datasourceconfiguration)" : DataSourceConfiguration,
      "[Description](#cfn-location-placeindex-description)" : String,
      "[IndexName](#cfn-location-placeindex-indexname)" : String,
      "[PricingPlan](#cfn-location-placeindex-pricingplan)" : String
    }
}
```

### YAML<a name="aws-resource-location-placeindex-syntax.yaml"></a>

```
Type: AWS::Location::PlaceIndex
Properties: 
  [DataSource](#cfn-location-placeindex-datasource): String
  [DataSourceConfiguration](#cfn-location-placeindex-datasourceconfiguration): 
    DataSourceConfiguration
  [Description](#cfn-location-placeindex-description): String
  [IndexName](#cfn-location-placeindex-indexname): String
  [PricingPlan](#cfn-location-placeindex-pricingplan): String
```

## Properties<a name="aws-resource-location-placeindex-properties"></a>

`DataSource`  <a name="cfn-location-placeindex-datasource"></a>
Specifies the geospatial data provider for the new place index\.  
This field is case\-sensitive\. Enter the valid values as shown\. For example, entering `HERE` returns an error\.
Valid values include:  
+ `Esri` – For additional information about [Esri](https://docs.aws.amazon.com/location/latest/developerguide/esri.html)'s coverage in your region of interest, see [Esri details on geocoding coverage](https://developers.arcgis.com/rest/geocode/api-reference/geocode-coverage.htm)\.
+ `Grab` – Grab provides place index functionality for Southeast Asia\. For additional information about [GrabMaps](https://docs.aws.amazon.com/location/latest/developerguide/grab.html)' coverage, see [GrabMaps countries and areas covered](https://docs.aws.amazon.com/location/latest/developerguide/grab.html#grab-coverage-area)\.
+ `Here` – For additional information about [HERE Technologies](https://docs.aws.amazon.com/location/latest/developerguide/HERE.html)' coverage in your region of interest, see [HERE details on goecoding coverage](https://developer.here.com/documentation/geocoder/dev_guide/topics/coverage-geocoder.html)\.
**Important**  
If you specify HERE Technologies \(`Here`\) as the data provider, you may not [store results](https://docs.aws.amazon.com/location-places/latest/APIReference/API_DataSourceConfiguration.html) for locations in Japan\. For more information, see the [AWS Service Terms](http://aws.amazon.com/service-terms/) for Amazon Location Service\.
For additional information , see [Data providers](https://docs.aws.amazon.com/location/latest/developerguide/what-is-data-provider.html) on the *Amazon Location Service Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSourceConfiguration`  <a name="cfn-location-placeindex-datasourceconfiguration"></a>
Specifies the data storage option requesting Places\.  
*Required*: No  
*Type*: [DataSourceConfiguration](aws-properties-location-placeindex-datasourceconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-location-placeindex-description"></a>
The optional description for the place index resource\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IndexName`  <a name="cfn-location-placeindex-indexname"></a>
The name of the place index resource\.   
Requirements:  
+ Contain only alphanumeric characters \(A–Z, a–z, 0–9\), hyphens \(\-\), periods \(\.\), and underscores \(\_\)\.
+ Must be a unique place index resource name\.
+ No spaces allowed\. For example, `ExamplePlaceIndex`\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[-._\w]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PricingPlan`  <a name="cfn-location-placeindex-pricingplan"></a>
No longer used\. If included, the only allowed value is `RequestBasedUsage`\.  
*Allowed Values*: `RequestBasedUsage`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-location-placeindex-return-values"></a>

### Ref<a name="aws-resource-location-placeindex-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `PlaceIndex` name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-location-placeindex-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-location-placeindex-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the place index resource\. Used to specify a resource across AWS\.   
+ Format example: `arn:aws:geo:region:account-id:place-index/ExamplePlaceIndex`

`CreateTime`  <a name="CreateTime-fn::getatt"></a>
The timestamp for when the place index resource was created in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.

`IndexArn`  <a name="IndexArn-fn::getatt"></a>
Synonym for `Arn`\. The Amazon Resource Name \(ARN\) for the place index resource\. Used to specify a resource across AWS\.   
+ Format example: `arn:aws:geo:region:account-id:place-index/ExamplePlaceIndex`

`UpdateTime`  <a name="UpdateTime-fn::getatt"></a>
The timestamp for when the place index resource was last updated in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.