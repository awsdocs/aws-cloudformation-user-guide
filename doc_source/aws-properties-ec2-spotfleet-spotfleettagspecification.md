# AWS::EC2::SpotFleet SpotFleetTagSpecification<a name="aws-properties-ec2-spotfleet-spotfleettagspecification"></a>

The tags for a Spot Fleet resource\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleettagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleettagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-spotfleet-spotfleettagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-spotfleet-spotfleettagspecification-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleettagspecification-syntax.yaml"></a>

```
  [ResourceType](#cfn-ec2-spotfleet-spotfleettagspecification-resourcetype): String
  [Tags](#cfn-ec2-spotfleet-spotfleettagspecification-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleettagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-spotfleet-spotfleettagspecification-resourcetype"></a>
The type of resource\. Currently, the only resource type that is supported is `instance`\. To tag the Spot Fleet request on creation, use the `TagSpecifications` parameter in [ `SpotFleetRequestConfigData` ](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SpotFleetRequestConfigData.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `capacity-reservation | carrier-gateway | client-vpn-endpoint | customer-gateway | dedicated-host | dhcp-options | egress-only-internet-gateway | elastic-gpu | elastic-ip | export-image-task | export-instance-task | fleet | fpga-image | host-reservation | image | import-image-task | import-snapshot-task | instance | instance-event-window | internet-gateway | ipv4pool-ec2 | ipv6pool-ec2 | key-pair | launch-template | local-gateway | local-gateway-route-table | local-gateway-route-table-virtual-interface-group-association | local-gateway-route-table-vpc-association | local-gateway-virtual-interface | local-gateway-virtual-interface-group | natgateway | network-acl | network-insights-analysis | network-insights-path | network-interface | placement-group | prefix-list | replace-root-volume-task | reserved-instances | route-table | security-group | security-group-rule | snapshot | spot-fleet-request | spot-instances-request | subnet | traffic-mirror-filter | traffic-mirror-session | traffic-mirror-target | transit-gateway | transit-gateway-attachment | transit-gateway-connect-peer | transit-gateway-multicast-domain | transit-gateway-route-table | volume | vpc | vpc-endpoint | vpc-endpoint-service | vpc-flow-log | vpc-peering-connection | vpn-connection | vpn-gateway`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-spotfleet-spotfleettagspecification-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)