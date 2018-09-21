# Amazon EC2 SpotFleet ClassicLoadBalancersConfig<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig"></a>

<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-description"></a>The `ClassicLoadBalancersConfig` property type specifies the Classic Load Balancers to attach to a Spot Fleet\. Spot Fleet registers the running Spot Instances with these Classic Load Balancers\.

<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-inheritance"></a> `ClassicLoadBalancersConfig` is a property of the [Amazon EC2 SpotFleet LoadBalancersConfig](aws-properties-ec2-spotfleet-loadbalancersconfig.md) property type\.

## Syntax<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-syntax.json"></a>

```
{
  "[ClassicLoadBalancers](#cfn-ec2-spotfleet-classicloadbalancersconfig-classicloadbalancers)" : [ [*ClassicLoadBalancer*](aws-properties-ec2-spotfleet-classicloadbalancer.md), ... ]
}
```

### YAML<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-syntax.yaml"></a>

```
[ClassicLoadBalancers](#cfn-ec2-spotfleet-classicloadbalancersconfig-classicloadbalancers)
  - [*ClassicLoadBalancer*](aws-properties-ec2-spotfleet-classicloadbalancer.md)
```

## Properties<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-properties"></a>

`ClassicLoadBalancers`  <a name="cfn-ec2-spotfleet-classicloadbalancersconfig-classicloadbalancers"></a>
One or more Classic Load Balancers to attach to the Spot Fleet\. Duplicates not allowed\. For property constraints, see [ClassicLoadBalancersConfig](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ClassicLoadBalancersConfig.html) in the *Amazon EC2 API Reference*\.  
 *Required*: Yes  
 *Type*: List of [Amazon EC2 SpotFleet ClassicLoadBalancer](aws-properties-ec2-spotfleet-classicloadbalancer.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-seealso"></a>
+ [ClassicLoadBalancersConfig](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ClassicLoadBalancersConfig.html) in the *Amazon EC2 API Reference*