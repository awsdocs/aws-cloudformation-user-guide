# AWS::ElasticLoadBalancingV2::ListenerRule<a name="aws-resource-elasticloadbalancingv2-listenerrule"></a>

The `AWS::ElasticLoadBalancingV2::ListenerRule` resource defines which requests an Elastic Load Balancing listener takes action on and the action that it takes\. For more information, see [Getting Started](http://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/load-balancer-getting-started.html) in the *Elastic Load Balancing User Guide*\.

**Topics**
+ [Syntax](#aws-resource-elasticloadbalancingv2-listenerrule-syntax)
+ [Properties](#w3ab2c21c10d644b9)
+ [Return Value](#w3ab2c21c10d644c11)
+ [Example](#w3ab2c21c10d644c13)

## Syntax<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::ListenerRule",
  "Properties" : {
    "[Actions](#cfn-elasticloadbalancingv2-listenerrule-actions)" : [ [Actions](aws-properties-elasticloadbalancingv2-listenerrule-actions.md), ... ],
    "[Conditions](#cfn-elasticloadbalancingv2-listenerrule-conditions)" : [ [Conditions](aws-properties-elasticloadbalancingv2-listenerrule-conditions.md), ... ],
    "[ListenerArn](#cfn-elasticloadbalancingv2-listenerrule-listenerarn)" : String,
    "[Priority](#cfn-elasticloadbalancingv2-listenerrule-priority)" : Integer
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax.yaml"></a>

```
Type: "AWS::ElasticLoadBalancingV2::ListenerRule"
Properties:
  [Actions](#cfn-elasticloadbalancingv2-listenerrule-actions):
    - [Actions](aws-properties-elasticloadbalancingv2-listenerrule-actions.md)
  [Conditions](#cfn-elasticloadbalancingv2-listenerrule-conditions):
    - [Conditions](aws-properties-elasticloadbalancingv2-listenerrule-conditions.md)
  [ListenerArn](#cfn-elasticloadbalancingv2-listenerrule-listenerarn): String
  [Priority](#cfn-elasticloadbalancingv2-listenerrule-priority): Integer
```

## Properties<a name="w3ab2c21c10d644b9"></a>

`Actions`  <a name="cfn-elasticloadbalancingv2-listenerrule-actions"></a>
The action that the listener takes when a request meets the specified condition\.  
*Required*: Yes  
*Type*: List of [Elastic Load Balancing ListenerRule Actions](aws-properties-elasticloadbalancingv2-listenerrule-actions.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Conditions`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions"></a>
The conditions under which a rule takes effect\.  
*Required*: Yes  
*Type*: List of [Elastic Load Balancing ListenerRule Conditions](aws-properties-elasticloadbalancingv2-listenerrule-conditions.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ListenerArn`  <a name="cfn-elasticloadbalancingv2-listenerrule-listenerarn"></a>
The Amazon Resource Name \(ARN\) of the listener that the rule applies to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Priority`  <a name="cfn-elasticloadbalancingv2-listenerrule-priority"></a>
The priority for the rule\. Elastic Load Balancing evaluates rules in priority order, from the lowest value to the highest value\. If a request satisfies a rule, Elastic Load Balancing ignores all subsequent rules\.  
A listener can have only one rule with a given priority\.
For valid values, see the `Priority` parameter for the [CreateRule](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateRule.html) action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d644c11"></a>

### Ref<a name="w3ab2c21c10d644c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the rule's ARN, such as `arn:aws:elasticloadbalancing:us-west-2:123456789012:listener-rule/app/my-load-balancer/50dc6c495c0c9188/f2f7dc8efc522ab2/9683b2d02a6cabee`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d644c13"></a>

The following example creates a rule that forwards requests to the `TargetGroup` target group if the request URL contains the `/img/*` pattern\.

### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule-example.json"></a>

```
"ListenerRule": {
  "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
  "Properties": {
    "Actions": [{
      "Type": "forward",
      "TargetGroupArn": { "Ref": "TargetGroup" }
    }],
    "Conditions": [{
      "Field": "path-pattern",
      "Values": [ "/img/*" ]
    }],
    "ListenerArn": { "Ref": "Listener" },
    "Priority": 1
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule-example.yaml"></a>

```
ListenerRule:
  Type: AWS::ElasticLoadBalancingV2::ListenerRule
  Properties:
    Actions:
    - Type: forward
      TargetGroupArn:
        Ref: TargetGroup
    Conditions:
    - Field: path-pattern
      Values:
      - "/img/*"
    ListenerArn:
      Ref: Listener
    Priority: 1
```