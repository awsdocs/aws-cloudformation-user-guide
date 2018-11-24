# Amazon EC2 SpotFleet LoadBalancersConfig<a name="aws-properties-ec2-spotfleet-loadbalancersconfig"></a>

<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-description"></a>The `LoadBalancersConfig` property type specifies the Classic Load Balancers and target groups to attach to a Spot Fleet request\.

<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-inheritance"></a> `LoadBalancersConfig` is a property of the [Amazon EC2 SpotFleet SpotFleetRequestConfigData](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata.md) property type\.

## Syntax<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-syntax.json"></a>

```
{
  "[ClassicLoadBalancersConfig](#cfn-ec2-spotfleet-loadbalancersconfig-classicloadbalancersconfig)" : [*ClassicLoadBalancersConfig*](aws-properties-ec2-spotfleet-classicloadbalancersconfig.md),
  "[TargetGroupsConfig](#cfn-ec2-spotfleet-loadbalancersconfig-targetgroupsconfig)" : [*TargetGroupsConfig*](aws-properties-ec2-spotfleet-targetgroupsconfig.md)
}
```

### YAML<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-syntax.yaml"></a>

```
[ClassicLoadBalancersConfig](#cfn-ec2-spotfleet-loadbalancersconfig-classicloadbalancersconfig): 
  [*ClassicLoadBalancersConfig*](aws-properties-ec2-spotfleet-classicloadbalancersconfig.md)
[TargetGroupsConfig](#cfn-ec2-spotfleet-loadbalancersconfig-targetgroupsconfig): 
  [*TargetGroupsConfig*](aws-properties-ec2-spotfleet-targetgroupsconfig.md)
```

## Properties<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-properties"></a>

`ClassicLoadBalancersConfig`  <a name="cfn-ec2-spotfleet-loadbalancersconfig-classicloadbalancersconfig"></a>
The Classic Load Balancers to attach to the SpotFleet request\.  
 *Required*: No  
 *Type*: [Amazon EC2 SpotFleet ClassicLoadBalancersConfig](aws-properties-ec2-spotfleet-classicloadbalancersconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetGroupsConfig`  <a name="cfn-ec2-spotfleet-loadbalancersconfig-targetgroupsconfig"></a>
The target groups to attach to the SpotFleet request\.  
 *Required*: No  
 *Type*: [Amazon EC2 SpotFleet TargetGroupsConfig](aws-properties-ec2-spotfleet-targetgroupsconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-seealso"></a>
+ [LoadBalancersConfig](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LoadBalancersConfig.html) in the *Amazon EC2 API Reference*