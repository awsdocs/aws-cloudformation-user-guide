# AWS::Grafana::Workspace NetworkAccessControl<a name="aws-properties-grafana-workspace-networkaccesscontrol"></a>

The configuration settings for in\-bound network access to your workspace\.

When this is configured, only listed IP addresses and VPC endpoints will be able to access your workspace\. Standard Grafana authentication and authorization are still required\.

Access is granted to a caller that is in either the IP address list or the VPC endpoint list \- they do not need to be in both\.

If this is not configured, or is removed, then all IP addresses and VPC endpoints are allowed\. Standard Grafana authentication and authorization are still required\.

**Note**  
While both `prefixListIds` and `vpceIds` are required, you can pass in an empty array of strings for either parameter if you do not want to allow any of that type\.  
If both are passed as empty arrays, no traffic is allowed to the workspace, because only *explicitly* allowed connections are accepted\.

## Syntax<a name="aws-properties-grafana-workspace-networkaccesscontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-grafana-workspace-networkaccesscontrol-syntax.json"></a>

```
{
  "[PrefixListIds](#cfn-grafana-workspace-networkaccesscontrol-prefixlistids)" : [ String, ... ],
  "[VpceIds](#cfn-grafana-workspace-networkaccesscontrol-vpceids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-grafana-workspace-networkaccesscontrol-syntax.yaml"></a>

```
  [PrefixListIds](#cfn-grafana-workspace-networkaccesscontrol-prefixlistids): 
    - String
  [VpceIds](#cfn-grafana-workspace-networkaccesscontrol-vpceids): 
    - String
```

## Properties<a name="aws-properties-grafana-workspace-networkaccesscontrol-properties"></a>

`PrefixListIds`  <a name="cfn-grafana-workspace-networkaccesscontrol-prefixlistids"></a>
An array of prefix list IDs\. A prefix list is a list of CIDR ranges of IP addresses\. The IP addresses specified are allowed to access your workspace\. If the list is not included in the configuration \(passed an empty array\) then no IP addresses are allowed to access the workspace\. You create a prefix list using the Amazon VPC console\.  
Prefix list IDs have the format `pl-1a2b3c4d`\.  
For more information about prefix lists, see [Group CIDR blocks using managed prefix lists](https://docs.aws.amazon.com/vpc/latest/userguide/managed-prefix-lists.html)in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpceIds`  <a name="cfn-grafana-workspace-networkaccesscontrol-vpceids"></a>
An array of Amazon VPC endpoint IDs for the workspace\. You can create VPC endpoints to your Amazon Managed Grafana workspace for access from within a VPC\. If a `NetworkAccessConfiguration` is specified then only VPC endpoints specified here are allowed to access the workspace\. If you pass in an empty array of strings, then no VPCs are allowed to access the workspace\.  
VPC endpoint IDs have the format `vpce-1a2b3c4d`\.  
For more information about creating an interface VPC endpoint, see [Interface VPC endpoints](https://docs.aws.amazon.com/grafana/latest/userguide/VPC-endpoints) in the *Amazon Managed Grafana User Guide*\.  
The only VPC endpoints that can be specified here are interface VPC endpoints for Grafana workspaces \(using the `com.amazonaws.[region].grafana-workspace` service endpoint\)\. Other VPC endpoints are ignored\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)