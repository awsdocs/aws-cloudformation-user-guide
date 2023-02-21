# AWS::Location::TrackerConsumer<a name="aws-resource-location-trackerconsumer"></a>

The `AWS::Location::TrackerConsumer` resource specifies an association between a geofence collection and a tracker resource\. The geofence collection is referred to as the *consumer* of the tracker\. This allows the tracker resource to communicate location data to the linked geofence collection\.

**Note**  
Currently not supported — Cross\-account configurations, such as creating associations between a tracker resource in one account and a geofence collection in another account\.

## Syntax<a name="aws-resource-location-trackerconsumer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-location-trackerconsumer-syntax.json"></a>

```
{
  "Type" : "AWS::Location::TrackerConsumer",
  "Properties" : {
      "[ConsumerArn](#cfn-location-trackerconsumer-consumerarn)" : String,
      "[TrackerName](#cfn-location-trackerconsumer-trackername)" : String
    }
}
```

### YAML<a name="aws-resource-location-trackerconsumer-syntax.yaml"></a>

```
Type: AWS::Location::TrackerConsumer
Properties: 
  [ConsumerArn](#cfn-location-trackerconsumer-consumerarn): String
  [TrackerName](#cfn-location-trackerconsumer-trackername): String
```

## Properties<a name="aws-resource-location-trackerconsumer-properties"></a>

`ConsumerArn`  <a name="cfn-location-trackerconsumer-consumerarn"></a>
The Amazon Resource Name \(ARN\) for the geofence collection to be associated to tracker resource\. Used when you need to specify a resource across all AWS\.  
+ Format example: `arn:aws:geo:region:account-id:geofence-collection/ExampleGeofenceCollectionConsumer`
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1600`  
*Pattern*: `^arn(:[a-z0-9]+([.-][a-z0-9]+)*){2}(:([a-z0-9]+([.-][a-z0-9]+)*)?){2}:([^/].*)?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TrackerName`  <a name="cfn-location-trackerconsumer-trackername"></a>
The name for the tracker resource\.  
Requirements:  
+ Contain only alphanumeric characters \(A\-Z, a\-z, 0\-9\) , hyphens \(\-\), periods \(\.\), and underscores \(\_\)\.
+ Must be a unique tracker resource name\.
+ No spaces allowed\. For example, `ExampleTracker`\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[-._\w]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-location-trackerconsumer-return-values"></a>

### Ref<a name="aws-resource-location-trackerconsumer-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `GeofenceCollection` name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.