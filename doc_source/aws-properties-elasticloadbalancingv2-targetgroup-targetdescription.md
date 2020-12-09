# AWS::ElasticLoadBalancingV2::TargetGroup TargetDescription<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription"></a>

Specifies a target to add to a target group\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone)" : String,
  "[Id](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-id)" : String,
  "[Port](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-port)" : Integer
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone): String
  [Id](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-id): String
  [Port](#cfn-elasticloadbalancingv2-targetgroup-targetdescription-port): Integer
```

## Properties<a name="aws-properties-elasticloadbalancingv2-targetgroup-targetdescription-properties"></a>

`AvailabilityZone`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetdescription-availabilityzone"></a>
An Availability Zone or `all`\. This determines whether the target receives traffic from the load balancer nodes in the specified Availability Zone or from all enabled Availability Zones for the load balancer\.  
This parameter is not supported if the target type of the target group is `instance`\.  
If the target type is `ip` and the IP address is in a subnet of the VPC for the target group, the Availability Zone is automatically detected and this parameter is optional\. If the IP address is outside the VPC, this parameter is required\.  
With an Application Load Balancer, if the target type is `ip` and the IP address is outside the VPC for the target group, the only supported value is `all`\.  
If the target type is `lambda`, this parameter is optional and the only supported value is `all`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetdescription-id"></a>
The ID of the target\. If the target type of the target group is `instance`, specify an instance ID\. If the target type is `ip`, specify an IP address\. If the target type is `lambda`, specify the ARN of the Lambda function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetdescription-port"></a>
The port on which the target is listening\. If the target group protocol is GENEVE, the supported port is 6081\. Not used if the target is a Lambda function\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)