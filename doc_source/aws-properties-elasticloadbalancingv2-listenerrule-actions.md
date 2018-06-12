# Elastic Load Balancing ListenerRule Actions<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions"></a>

`Actions` is a property of the [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md) resource that specifies the actions an Elastic Load Balancing listener takes when an incoming request meets a listener rule's condition\.

## Syntax<a name="w3ab2c21c14e1012b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions-syntax.json"></a>

```
{
  "[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-actions-targetgrouparn)" : String,
  "[Type](#cfn-elasticloadbalancingv2-listener-actions-type)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions-syntax.yaml"></a>

```
[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-actions-targetgrouparn): String
[Type](#cfn-elasticloadbalancingv2-listener-actions-type): String
```

## Properties<a name="w3ab2c21c14e1012b7"></a>

`TargetGroupArn`  <a name="cfn-elasticloadbalancingv2-listener-actions-targetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the target group to which Elastic Load Balancing routes the traffic\.  
*Required*: Yes  
*Type*: String

`Type`  <a name="cfn-elasticloadbalancingv2-listener-actions-type"></a>
The type of action\. For valid values, see the `Type` contents for the [Action](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_Action.html) data type in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: Yes  
*Type*: String