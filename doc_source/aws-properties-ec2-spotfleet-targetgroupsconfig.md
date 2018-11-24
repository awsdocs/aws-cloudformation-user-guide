# Amazon EC2 SpotFleet TargetGroupsConfig<a name="aws-properties-ec2-spotfleet-targetgroupsconfig"></a>

<a name="aws-properties-ec2-spotfleet-targetgroupsconfig-description"></a>The `TargetGroupsConfig` property type describes the target groups to attach to a Spot Fleet\. Spot Fleet registers the running Spot Instances with these target groups\.

<a name="aws-properties-ec2-spotfleet-targetgroupsconfig-inheritance"></a> `TargetGroupsConfig` is a property of the [Amazon EC2 SpotFleet LoadBalancersConfig](aws-properties-ec2-spotfleet-loadbalancersconfig.md) property type\.

## Syntax<a name="aws-properties-ec2-spotfleet-targetgroupsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-targetgroupsconfig-syntax.json"></a>

```
{
  "[TargetGroups](#cfn-ec2-spotfleet-targetgroupsconfig-targetgroups)" : [ [*TargetGroup*](aws-properties-ec2-spotfleet-targetgroup.md), ... ]
}
```

### YAML<a name="aws-properties-ec2-spotfleet-targetgroupsconfig-syntax.yaml"></a>

```
[TargetGroups](#cfn-ec2-spotfleet-targetgroupsconfig-targetgroups):
  - [*TargetGroup*](aws-properties-ec2-spotfleet-targetgroup.md)
```

## Properties<a name="aws-properties-ec2-spotfleet-targetgroupsconfig-properties"></a>

`TargetGroups`  <a name="cfn-ec2-spotfleet-targetgroupsconfig-targetgroups"></a>
One or more target groups\. Duplicates not allowed\. For property constraints, see [TargetGroupsConfig](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_TargetGroupsConfig.html) in the *Amazon EC2 API Reference*  
 *Required*: Yes  
 *Type*: List of [Amazon EC2 SpotFleet TargetGroup](aws-properties-ec2-spotfleet-targetgroup.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-spotfleet-targetgroupsconfig-seealso"></a>
+ [TargetGroupsConfig](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_TargetGroupsConfig.html) in the *Amazon EC2 API Reference*