# AWS::Location::GeofenceCollection<a name="aws-resource-location-geofencecollection"></a>

The `AWS::Location::GeofenceCollection` resource specifies the ability to detect and act when a tracked device enters or exits a defined geographical boundary known as a geofence\.

## Syntax<a name="aws-resource-location-geofencecollection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-location-geofencecollection-syntax.json"></a>

```
{
  "Type" : "AWS::Location::GeofenceCollection",
  "Properties" : {
      "[CollectionName](#cfn-location-geofencecollection-collectionname)" : String,
      "[Description](#cfn-location-geofencecollection-description)" : String,
      "[KmsKeyId](#cfn-location-geofencecollection-kmskeyid)" : String,
      "[PricingPlan](#cfn-location-geofencecollection-pricingplan)" : String,
      "[PricingPlanDataSource](#cfn-location-geofencecollection-pricingplandatasource)" : String
    }
}
```

### YAML<a name="aws-resource-location-geofencecollection-syntax.yaml"></a>

```
Type: AWS::Location::GeofenceCollection
Properties: 
  [CollectionName](#cfn-location-geofencecollection-collectionname): String
  [Description](#cfn-location-geofencecollection-description): String
  [KmsKeyId](#cfn-location-geofencecollection-kmskeyid): String
  [PricingPlan](#cfn-location-geofencecollection-pricingplan): String
  [PricingPlanDataSource](#cfn-location-geofencecollection-pricingplandatasource): String
```

## Properties<a name="aws-resource-location-geofencecollection-properties"></a>

`CollectionName`  <a name="cfn-location-geofencecollection-collectionname"></a>
The name for the geofence collection\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[-._\w]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-location-geofencecollection-description"></a>
An optional description for the geofence collection\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-location-geofencecollection-kmskeyid"></a>
A key identifier for an [AWS KMS customer managed key](https://docs.aws.amazon.com/kms/latest/developerguide/create-keys.html)\. Enter a key ID, key ARN, alias name, or alias ARN\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PricingPlan`  <a name="cfn-location-geofencecollection-pricingplan"></a>
Specifies the pricing plan for the geofence collection\.  
For additional details and restrictions on each pricing plan option, see the [Amazon Location Service pricing page](http://aws.amazon.com/location/pricing/)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MobileAssetManagement | MobileAssetTracking | RequestBasedUsage`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PricingPlanDataSource`  <a name="cfn-location-geofencecollection-pricingplandatasource"></a>
Specifies the data provider for the geofence collection\.  
+ Required value for the following pricing plans: `MobileAssetTracking` \| `MobileAssetManagement`
For more information about [Data Providers](http://aws.amazon.com/location/data-providers/), and [Pricing plans](http://aws.amazon.com/location/pricing/), see the Amazon Location Service product page\.  
Amazon Location Service only uses `PricingPlanDataSource` to calculate billing for your geofence collection\. Your data will not be shared with the data provider, and will remain in your AWS account or region unless you move it\.
Valid Values: `Esri` \| `Here`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-location-geofencecollection-return-values"></a>

### Ref<a name="aws-resource-location-geofencecollection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `GeofenceCollection` ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-location-geofencecollection-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-location-geofencecollection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the geofence collection resource\. Used when you need to specify a resource across all AWS\.  
+ Format example: `arn:aws:geo:region:account-id:geofence-collection/ExampleGeofenceCollection`

`CollectionArn`  <a name="CollectionArn-fn::getatt"></a>
Synonym for `Arn`\. The Amazon Resource Name \(ARN\) for the geofence collection resource\. Used when you need to specify a resource across all AWS\.  
+ Format example: `arn:aws:geo:region:account-id:geofence-collection/ExampleGeofenceCollection`

`CreateTime`  <a name="CreateTime-fn::getatt"></a>
The timestamp for when the geofence collection resource was created in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.

`UpdateTime`  <a name="UpdateTime-fn::getatt"></a>
The timestamp for when the geofence collection resource was last updated in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.