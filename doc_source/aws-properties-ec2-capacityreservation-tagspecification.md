# Amazon EC2 CapacityReservation TagSpecification<a name="aws-properties-ec2-capacityreservation-tagspecification"></a>

<a name="aws-properties-ec2-capacityreservation-tagspecification-description"></a>The `TagSpecification` property type specifies the tags specification for an Amazon EC2 Capacity Reservation\.

<a name="aws-properties-ec2-capacityreservation-tagspecification-inheritance"></a> `TagSpecification` is a property of the [AWS::EC2::CapacityReservation](aws-resource-ec2-capacityreservation.md) resource\.

## Syntax<a name="aws-properties-ec2-capacityreservation-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-capacityreservation-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-capacityreservation-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-capacityreservation-tagspecification-tags)" : [ [*Tag*](aws-properties-ec2-capacityreservation-tag.md), ... ]
}
```

### YAML<a name="aws-properties-ec2-capacityreservation-tagspecification-syntax.yaml"></a>

```
[ResourceType](#cfn-ec2-capacityreservation-tagspecification-resourcetype): String
  [Tags](#cfn-ec2-capacityreservation-tagspecification-tags): 
    - [*Tag*](aws-properties-ec2-capacityreservation-tag.md)
```

## Properties<a name="aws-properties-ec2-capacityreservation-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-capacityreservation-tagspecification-resourcetype"></a>
The type of resource to tag\. To tag an Amazon EC2 Capacity Reservation, specify `capacity-reservation`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-ec2-capacityreservation-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: No  
*Type*: List of [Tag](aws-properties-ec2-capacityreservation-tag.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-ec2-capacityreservation-tagspecification-seealso"></a>
+ [TagSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_TagSpecification.html) in the *Amazon EC2 API Reference*\.