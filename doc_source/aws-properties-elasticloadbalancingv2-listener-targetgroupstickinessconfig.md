# AWS::ElasticLoadBalancingV2::Listener TargetGroupStickinessConfig<a name="aws-properties-elasticloadbalancingv2-listener-targetgroupstickinessconfig"></a>

Information about the target group stickiness for a rule\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-targetgroupstickinessconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-targetgroupstickinessconfig-syntax.json"></a>

```
{
  "[DurationSeconds](#cfn-elasticloadbalancingv2-listener-targetgroupstickinessconfig-durationseconds)" : Integer,
  "[Enabled](#cfn-elasticloadbalancingv2-listener-targetgroupstickinessconfig-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-targetgroupstickinessconfig-syntax.yaml"></a>

```
  [DurationSeconds](#cfn-elasticloadbalancingv2-listener-targetgroupstickinessconfig-durationseconds): Integer
  [Enabled](#cfn-elasticloadbalancingv2-listener-targetgroupstickinessconfig-enabled): Boolean
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-targetgroupstickinessconfig-properties"></a>

`DurationSeconds`  <a name="cfn-elasticloadbalancingv2-listener-targetgroupstickinessconfig-durationseconds"></a>
The time period, in seconds, during which requests from a client should be routed to the same target group\. The range is 1\-604800 seconds \(7 days\)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-elasticloadbalancingv2-listener-targetgroupstickinessconfig-enabled"></a>
Indicates whether target group stickiness is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)