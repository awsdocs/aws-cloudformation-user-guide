# AWS::EC2::ClientVpnEndpoint TagSpecification<a name="aws-properties-ec2-clientvpnendpoint-tagspecification"></a>

The tags to apply to a resource when the resource is being created\.

## Syntax<a name="aws-properties-ec2-clientvpnendpoint-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-clientvpnendpoint-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-clientvpnendpoint-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-clientvpnendpoint-tagspecification-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-ec2-clientvpnendpoint-tagspecification-syntax.yaml"></a>

```
  [ResourceType](#cfn-ec2-clientvpnendpoint-tagspecification-resourcetype): String
  [Tags](#cfn-ec2-clientvpnendpoint-tagspecification-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-clientvpnendpoint-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-clientvpnendpoint-tagspecification-resourcetype"></a>
The type of resource to tag\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `client-vpn-endpoint | customer-gateway | dedicated-host | dhcp-options | egress-only-internet-gateway | elastic-gpu | elastic-ip | export-image-task | export-instance-task | fleet | fpga-image | host-reservation | image | import-image-task | import-snapshot-task | instance | internet-gateway | key-pair | launch-template | local-gateway-route-table-vpc-association | natgateway | network-acl | network-interface | placement-group | reserved-instances | route-table | security-group | snapshot | spot-fleet-request | spot-instances-request | subnet | traffic-mirror-filter | traffic-mirror-session | traffic-mirror-target | transit-gateway | transit-gateway-attachment | transit-gateway-multicast-domain | transit-gateway-route-table | volume | vpc | vpc-flow-log | vpc-peering-connection | vpn-connection | vpn-gateway`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-clientvpnendpoint-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: Yes  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)