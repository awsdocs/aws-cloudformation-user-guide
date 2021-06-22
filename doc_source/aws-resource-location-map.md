# AWS::Location::Map<a name="aws-resource-location-map"></a>

The `AWS::Location::Map` resource specifies a map resource in your AWS account, which provides map tiles of different styles sourced from global location data providers\.

## Syntax<a name="aws-resource-location-map-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-location-map-syntax.json"></a>

```
{
  "Type" : "AWS::Location::Map",
  "Properties" : {
      "[Configuration](#cfn-location-map-configuration)" : MapConfiguration,
      "[Description](#cfn-location-map-description)" : String,
      "[MapName](#cfn-location-map-mapname)" : String,
      "[PricingPlan](#cfn-location-map-pricingplan)" : String
    }
}
```

### YAML<a name="aws-resource-location-map-syntax.yaml"></a>

```
Type: AWS::Location::Map
Properties: 
  [Configuration](#cfn-location-map-configuration): 
    MapConfiguration
  [Description](#cfn-location-map-description): String
  [MapName](#cfn-location-map-mapname): String
  [PricingPlan](#cfn-location-map-pricingplan): String
```

## Properties<a name="aws-resource-location-map-properties"></a>

`Configuration`  <a name="cfn-location-map-configuration"></a>
Specifies the map style selected from an available data provider\.  
*Required*: Yes  
*Type*: [MapConfiguration](aws-properties-location-map-mapconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-location-map-description"></a>
An optional description for the map resource\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MapName`  <a name="cfn-location-map-mapname"></a>
The name for the map resource\.  
Requirements:  
+ Must contain only alphanumeric characters \(A–Z, a–z, 0–9\), hyphens \(\-\), periods \(\.\), and underscores \(\_\)\.
+ Must be a unique map resource name\.
+ No spaces allowed\. For example, `ExampleMap`\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[-._\w]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PricingPlan`  <a name="cfn-location-map-pricingplan"></a>
Specifies the pricing plan for your map resource\.  
For additional details and restrictions on each pricing plan option, see the [Amazon Location Service pricing page](https://docs.aws.amazon.com/location/pricing/)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MobileAssetManagement | MobileAssetTracking | RequestBasedUsage`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-location-map-return-values"></a>

### Ref<a name="aws-resource-location-map-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-location-map-return-values-fn--getatt"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `MapName`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

#### <a name="aws-resource-location-map-return-values-fn--getatt-fn--getatt"></a>

`DataSource`  <a name="DataSource-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`UpdateTime`  <a name="UpdateTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.