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
Specifies the `MapConfiguration`, including the map style, for the map resource that you create\. The map style defines the look of maps and the data provider for your map resource\.  
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
No longer used\. If included, the only allowed value is `RequestBasedUsage`\.  
*Allowed Values*: `RequestBasedUsage`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-location-map-return-values"></a>

### Ref<a name="aws-resource-location-map-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Map` name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-location-map-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-location-map-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the map resource\. Used to specify a resource across all AWS\.  
+ Format example: `arn:aws:geo:region:account-id:maps/ExampleMap`

`CreateTime`  <a name="CreateTime-fn::getatt"></a>
The timestamp for when the map resource was created in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.

`DataSource`  <a name="DataSource-fn::getatt"></a>
The data provider for the associated map tiles\.

`MapArn`  <a name="MapArn-fn::getatt"></a>
Synonym for `Arn`\. The Amazon Resource Name \(ARN\) for the map resource\. Used to specify a resource across all AWS\.  
+ Format example: `arn:aws:geo:region:account-id:maps/ExampleMap`

`UpdateTime`  <a name="UpdateTime-fn::getatt"></a>
The timestamp for when the map resource was last updated in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.