# AWS::EC2::SpotFleet LoadBalancersConfig<a name="aws-properties-ec2-spotfleet-loadbalancersconfig"></a>

Specifies the Classic Load Balancers and target groups to attach to a Spot Fleet request\.

## Syntax<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-syntax.json"></a>

```
{
  "[ClassicLoadBalancersConfig](#cfn-ec2-spotfleet-loadbalancersconfig-classicloadbalancersconfig)" : ClassicLoadBalancersConfig,
  "[TargetGroupsConfig](#cfn-ec2-spotfleet-loadbalancersconfig-targetgroupsconfig)" : TargetGroupsConfig
}
```

### YAML<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-syntax.yaml"></a>

```
  [ClassicLoadBalancersConfig](#cfn-ec2-spotfleet-loadbalancersconfig-classicloadbalancersconfig): 
    ClassicLoadBalancersConfig
  [TargetGroupsConfig](#cfn-ec2-spotfleet-loadbalancersconfig-targetgroupsconfig): 
    TargetGroupsConfig
```

## Properties<a name="aws-properties-ec2-spotfleet-loadbalancersconfig-properties"></a>

`ClassicLoadBalancersConfig`  <a name="cfn-ec2-spotfleet-loadbalancersconfig-classicloadbalancersconfig"></a>
The Classic Load Balancers\.  
*Required*: No  
*Type*: [ClassicLoadBalancersConfig](aws-properties-ec2-spotfleet-classicloadbalancersconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupsConfig`  <a name="cfn-ec2-spotfleet-loadbalancersconfig-targetgroupsconfig"></a>
The target groups\.  
*Required*: No  
*Type*: [TargetGroupsConfig](aws-properties-ec2-spotfleet-targetgroupsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)