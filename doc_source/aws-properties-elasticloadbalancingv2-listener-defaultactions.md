# Elastic Load Balancing Listener Action<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions"></a>

The `Action` property type specifies the default actions that the Elastic Load Balancing listener takes when handling incoming requests\.

The `DefaultActions` property of the [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md) resource contains a list of `Action` property types\.

## Syntax<a name="w4ab1c21c14e1100b7"></a>

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-syntax.json"></a>

```
{
  "[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn)" : String,
  "[Type](#cfn-elasticloadbalancingv2-listener-defaultactions-type)" : String
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-defaultactions-syntax.yaml"></a>

```
[TargetGroupArn](#cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn): String
[Type](#cfn-elasticloadbalancingv2-listener-defaultactions-type): String
```

## Properties<a name="w4ab1c21c14e1100b9"></a>

`TargetGroupArn`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions-targetgrouparn"></a>
The Amazon Resource Name \(ARN\) of the target group to which Elastic Load Balancing routes the traffic\.  
*Required*: Yes  
*Type*: String

`Type`  <a name="cfn-elasticloadbalancingv2-listener-defaultactions-type"></a>
The type of action\.  
*Valid values*: `forward`  
*Required*: Yes  
*Type*: String