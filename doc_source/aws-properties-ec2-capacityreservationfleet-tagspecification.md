# AWS::EC2::CapacityReservationFleet TagSpecification<a name="aws-properties-ec2-capacityreservationfleet-tagspecification"></a>

The tags to apply to a resource when the resource is being created\. When you specify a tag, you must specify the resource type to tag, otherwise the request will fail\.

**Note**  
The `Valid Values` lists all the resource types that can be tagged\. However, the action you're using might not support tagging all of these resource types\. If you try to tag a resource type that is unsupported for the action you're using, you'll get an error\.

## Syntax<a name="aws-properties-ec2-capacityreservationfleet-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-capacityreservationfleet-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-capacityreservationfleet-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-capacityreservationfleet-tagspecification-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-ec2-capacityreservationfleet-tagspecification-syntax.yaml"></a>

```
  [ResourceType](#cfn-ec2-capacityreservationfleet-tagspecification-resourcetype): String
  [Tags](#cfn-ec2-capacityreservationfleet-tagspecification-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-capacityreservationfleet-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-capacityreservationfleet-tagspecification-resourcetype"></a>
The type of resource to tag on creation\. Specify `capacity-reservation-fleet`\.  
To tag a resource after it has been created, see [CreateTags](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateTags.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-capacityreservationfleet-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)