# AWS::EC2::ClientVpnEndpoint TagSpecification<a name="aws-properties-ec2-clientvpnendpoint-tagspecification"></a>

The tags to apply to a resource when the resource is being created\. When you specify a tag, you must specify the resource type to tag, otherwise the request will fail\.

**Note**  
The `Valid Values` lists all the resource types that can be tagged\. However, the action you're using might not support tagging all of these resource types\. If you try to tag a resource type that is unsupported for the action you're using, you'll get an error\.

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
*Allowed values*: `capacity-reservation | capacity-reservation-fleet | carrier-gateway | client-vpn-endpoint | coip-pool | customer-gateway | dedicated-host | dhcp-options | egress-only-internet-gateway | elastic-gpu | elastic-ip | export-image-task | export-instance-task | fleet | fpga-image | host-reservation | image | import-image-task | import-snapshot-task | instance | instance-event-window | internet-gateway | ipam | ipam-pool | ipam-resource-discovery | ipam-resource-discovery-association | ipam-scope | ipv4pool-ec2 | ipv6pool-ec2 | key-pair | launch-template | local-gateway | local-gateway-route-table | local-gateway-route-table-virtual-interface-group-association | local-gateway-route-table-vpc-association | local-gateway-virtual-interface | local-gateway-virtual-interface-group | natgateway | network-acl | network-insights-access-scope | network-insights-access-scope-analysis | network-insights-analysis | network-insights-path | network-interface | placement-group | prefix-list | replace-root-volume-task | reserved-instances | route-table | security-group | security-group-rule | snapshot | spot-fleet-request | spot-instances-request | subnet | subnet-cidr-reservation | traffic-mirror-filter | traffic-mirror-filter-rule | traffic-mirror-session | traffic-mirror-target | transit-gateway | transit-gateway-attachment | transit-gateway-connect-peer | transit-gateway-multicast-domain | transit-gateway-policy-table | transit-gateway-route-table | transit-gateway-route-table-announcement | verified-access-endpoint | verified-access-group | verified-access-instance | verified-access-policy | verified-access-trust-provider | volume | vpc | vpc-block-public-access-exclusion | vpc-endpoint | vpc-endpoint-connection | vpc-endpoint-connection-device-type | vpc-endpoint-service | vpc-endpoint-service-permission | vpc-flow-log | vpc-peering-connection | vpn-connection | vpn-connection-device-type | vpn-gateway`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-clientvpnendpoint-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: Yes  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)