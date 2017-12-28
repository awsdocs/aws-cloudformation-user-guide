# Elastic Load Balancing ListenerRule Actions<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions"></a>

`Actions` is a property of the [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md) resource that specifies the actions an Elastic Load Balancing listener takes when an incoming request meets a listener rule's condition\.

## Syntax<a name="w3ab2c21c14d825b5"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-actions-targetgrouparn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-actions-type)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listenerrule-actions-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-actions-targetgrouparn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-listener-actions-type): String
```

## Properties<a name="w3ab2c21c14d825b7"></a>

`TargetGroupArn`  
The Amazon Resource Name \(ARN\) of the target group to which Elastic Load Balancing routes the traffic\.  
*Required: *Yes  
*Type*: String

`Type`  
The type of action\. For valid values, see the `Type` contents for the [Action](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_Action.html) data type in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *Yes  
*Type*: String