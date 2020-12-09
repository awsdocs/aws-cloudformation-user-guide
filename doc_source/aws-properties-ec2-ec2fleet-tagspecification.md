# AWS::EC2::EC2Fleet TagSpecification<a name="aws-properties-ec2-ec2fleet-tagspecification"></a>

Specifies the tags to apply to a resource when the resource is being created for an EC2 Fleet\.

 `TagSpecification` is a property of the [ AWS::EC2::EC2Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-ec2fleet.html) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-ec2fleet-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-ec2fleet-tagspecification-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-tagspecification-syntax.yaml"></a>

```
  [ResourceType](#cfn-ec2-ec2fleet-tagspecification-resourcetype): String
  [Tags](#cfn-ec2-ec2fleet-tagspecification-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-ec2fleet-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-ec2fleet-tagspecification-resourcetype"></a>
The type of resource to tag\. `ResourceType` must be `fleet`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `client-vpn-endpoint | customer-gateway | dedicated-host | dhcp-options | egress-only-internet-gateway | elastic-gpu | elastic-ip | export-image-task | export-instance-task | fleet | fpga-image | host-reservation | image | import-image-task | import-snapshot-task | instance | internet-gateway | key-pair | launch-template | local-gateway-route-table-vpc-association | natgateway | network-acl | network-interface | placement-group | reserved-instances | route-table | security-group | snapshot | spot-fleet-request | spot-instances-request | subnet | traffic-mirror-filter | traffic-mirror-session | traffic-mirror-target | transit-gateway | transit-gateway-attachment | transit-gateway-multicast-domain | transit-gateway-route-table | volume | vpc | vpc-flow-log | vpc-peering-connection | vpn-connection | vpn-gateway`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-ec2fleet-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-ec2-ec2fleet-tagspecification--seealso"></a>
+  [ TagSpecification](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_TagSpecification.html) in the *Amazon EC2 API Reference*