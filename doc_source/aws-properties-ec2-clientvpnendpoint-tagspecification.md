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
*Required*: No  
*Type*: String  
*Allowed Values*: `client-vpn-endpoint | customer-gateway | dedicated-host | dhcp-options | elastic-ip | fleet | fpga-image | host-reservation | image | instance | internet-gateway | launch-template | natgateway | network-acl | network-interface | reserved-instances | route-table | security-group | snapshot | spot-instances-request | subnet | transit-gateway | transit-gateway-attachment | transit-gateway-route-table | volume | vpc | vpc-peering-connection | vpn-connection | vpn-gateway`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-clientvpnendpoint-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)