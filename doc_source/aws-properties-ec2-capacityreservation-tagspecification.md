# AWS::EC2::CapacityReservation TagSpecification<a name="aws-properties-ec2-capacityreservation-tagspecification"></a>

An array of key\-value pairs to apply to this resource\.

For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.

## Syntax<a name="aws-properties-ec2-capacityreservation-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-capacityreservation-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-capacityreservation-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-capacityreservation-tagspecification-tags)" : [ [Tag](aws-properties-ec2-capacityreservation-tag.md), ... ]
}
```

### YAML<a name="aws-properties-ec2-capacityreservation-tagspecification-syntax.yaml"></a>

```
  [ResourceType](#cfn-ec2-capacityreservation-tagspecification-resourcetype): String
  [Tags](#cfn-ec2-capacityreservation-tagspecification-tags): 
    - [Tag](aws-properties-ec2-capacityreservation-tag.md)
```

## Properties<a name="aws-properties-ec2-capacityreservation-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-capacityreservation-tagspecification-resourcetype"></a>
The type of resource to tag\. Specify `capacity-reservation`\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `client-vpn-endpoint | customer-gateway | dedicated-host | dhcp-options | elastic-ip | fleet | fpga-image | host-reservation | image | instance | internet-gateway | launch-template | natgateway | network-acl | network-interface | reserved-instances | route-table | security-group | snapshot | spot-instances-request | subnet | transit-gateway | transit-gateway-attachment | transit-gateway-route-table | volume | vpc | vpc-peering-connection | vpn-connection | vpn-gateway`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-capacityreservation-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: No  
*Type*: List of [Tag](aws-properties-ec2-capacityreservation-tag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)