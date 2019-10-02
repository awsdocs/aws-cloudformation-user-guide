# AWS::ElasticLoadBalancingV2::LoadBalancer SubnetMapping<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping"></a>

Specifies a subnet to attach to an Application Load Balancer or a Network Load Balancer\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-syntax.json"></a>

```
{
  "[AllocationId](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-allocationid)" : String,
  "[SubnetId](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-subnetid)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-syntax.yaml"></a>

```
  [AllocationId](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-allocationid): String
  [SubnetId](#cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-subnetid): String
```

## Properties<a name="aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping-properties"></a>

`AllocationId`  <a name="cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-allocationid"></a>
\[Network Load Balancers\] The allocation ID of the Elastic IP address\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-elasticloadbalancingv2-loadbalancer-subnetmapping-subnetid"></a>
The ID of the subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by ***all*** regions.