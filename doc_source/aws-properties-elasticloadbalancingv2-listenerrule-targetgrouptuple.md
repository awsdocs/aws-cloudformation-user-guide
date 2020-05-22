# AWS::ElasticLoadBalancingV2::ListenerRule TargetGroupTuple<a name="aws-properties-elasticloadbalancingv2-listenerrule-targetgrouptuple"></a>

Information about how traffic will be distributed between multiple target groups in a forward rule\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listenerrule-targetgrouptuple-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-targetgrouptuple-syntax.json"></a>

```
{
  "[TargetGroupArn](#cfn-elasticloadbalancingv2-listenerrule-targetgrouptuple-targetgrouparn)" : String,
  "[Weight](#cfn-elasticloadbalancingv2-listenerrule-targetgrouptuple-weight)" : Integer
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-targetgrouptuple-syntax.yaml"></a>

```
  [TargetGroupArn](#cfn-elasticloadbalancingv2-listenerrule-targetgrouptuple-targetgrouparn): String
  [Weight](#cfn-elasticloadbalancingv2-listenerrule-targetgrouptuple-weight): Integer
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listenerrule-targetgrouptuple-properties"></a>

`TargetGroupArn`  <a name="cfn-elasticloadbalancingv2-listenerrule-targetgrouptuple-targetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the target group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-elasticloadbalancingv2-listenerrule-targetgrouptuple-weight"></a>
The weight\. The range is 0 to 999\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)