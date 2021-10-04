# AWS::Location::PlaceIndex<a name="aws-resource-location-placeindex"></a>

The `AWS::Location::PlaceIndex` resource specifies a place index resource in your AWS account, which supports Places functions with geospatial data sourced from your chosen data provider\.

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
Specifies the data provider of geospatial data\.  
This field is case\-sensitive\. Enter the valid values as shown\. For example, entering `HERE` will return an error\.
Valid values include:  
+ `Esri`
+ `Here`
**Important**  
Place index resources using HERE as a data provider can't be used to [store](https://docs.aws.amazon.com/location-places/latest/APIReference/API_DataSourceConfiguration.html) results for locations in Japan\. For more information, see the [AWS Service Terms](https://docs.aws.amazon.com/service-terms/) for Amazon Location Service\.
For additional details on data providers, see the [Amazon Location Service data providers page](https://docs.aws.amazon.com/location/latest/developerguide/what-is-data-provider.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSourceConfiguration`  <a name="cfn-location-placeindex-datasourceconfiguration"></a>
Specifies the data storage option for requesting Places\.  
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
Specifies the pricing plan for your place index resource\.  
For additional details and restrictions on each pricing plan option, see the [Amazon Location Service pricing page](https://docs.aws.amazon.com/location/pricing/)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MobileAssetManagement | MobileAssetTracking | RequestBasedUsage`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)