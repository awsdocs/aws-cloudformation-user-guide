# AWS::EC2::LaunchTemplate LaunchTemplateTagSpecification<a name="aws-properties-ec2-launchtemplate-launchtemplatetagspecification"></a>

Specifies the tags to apply to the launch template during creation\.

`LaunchTemplateTagSpecification` is a property of [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatetagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatetagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-launchtemplate-launchtemplatetagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-launchtemplate-launchtemplatetagspecification-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatetagspecification-syntax.yaml"></a>

```
  [ResourceType](#cfn-ec2-launchtemplate-launchtemplatetagspecification-resourcetype): String
  [Tags](#cfn-ec2-launchtemplate-launchtemplatetagspecification-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatetagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-launchtemplate-launchtemplatetagspecification-resourcetype"></a>
The type of resource\. To tag the launch template, `ResourceType` must be `launch-template`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `client-vpn-endpoint | customer-gateway | dedicated-host | dhcp-options | egress-only-internet-gateway | elastic-gpu | elastic-ip | export-image-task | export-instance-task | fleet | fpga-image | host-reservation | image | import-image-task | import-snapshot-task | instance | instance-event-window | internet-gateway | key-pair | launch-template | local-gateway-route-table-vpc-association | natgateway | network-acl | network-insights-analysis | network-insights-path | network-interface | placement-group | reserved-instances | route-table | security-group | security-group-rule | snapshot | spot-fleet-request | spot-instances-request | subnet | traffic-mirror-filter | traffic-mirror-session | traffic-mirror-target | transit-gateway | transit-gateway-attachment | transit-gateway-connect-peer | transit-gateway-multicast-domain | transit-gateway-route-table | volume | vpc | vpc-flow-log | vpc-peering-connection | vpn-connection | vpn-gateway`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-launchtemplate-launchtemplatetagspecification-tags"></a>
The tags for the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)