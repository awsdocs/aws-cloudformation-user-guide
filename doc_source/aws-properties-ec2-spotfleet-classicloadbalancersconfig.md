# AWS::EC2::SpotFleet ClassicLoadBalancersConfig<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig"></a>

Specifies the Classic Load Balancers to attach to a Spot Fleet\. Spot Fleet registers the running Spot Instances with these Classic Load Balancers\.

## Syntax<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-syntax.json"></a>

```
{
  "[ClassicLoadBalancers](#cfn-ec2-spotfleet-classicloadbalancersconfig-classicloadbalancers)" : [ ClassicLoadBalancer, ... ]
}
```

### YAML<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-syntax.yaml"></a>

```
  [ClassicLoadBalancers](#cfn-ec2-spotfleet-classicloadbalancersconfig-classicloadbalancers): 
    - ClassicLoadBalancer
```

## Properties<a name="aws-properties-ec2-spotfleet-classicloadbalancersconfig-properties"></a>

`ClassicLoadBalancers`  <a name="cfn-ec2-spotfleet-classicloadbalancersconfig-classicloadbalancers"></a>
One or more Classic Load Balancers\.  
*Required*: Yes  
*Type*: List of [ClassicLoadBalancer](aws-properties-ec2-spotfleet-classicloadbalancer.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)