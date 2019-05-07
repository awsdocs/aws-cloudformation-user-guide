# AWS::ElasticLoadBalancingV2::ListenerRule<a name="aws-resource-elasticloadbalancingv2-listenerrule"></a>

Specifies a listener rule\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::ListenerRule",
  "Properties" : {
      "[Actions](#cfn-elasticloadbalancingv2-listenerrule-actions)" : [ [Action](aws-properties-elasticloadbalancingv2-listenerrule-actions.md), ... ],
      "[Conditions](#cfn-elasticloadbalancingv2-listenerrule-conditions)" : [ [RuleCondition](aws-properties-elasticloadbalancingv2-listenerrule-conditions.md), ... ],
      "[ListenerArn](#cfn-elasticloadbalancingv2-listenerrule-listenerarn)" : String,
      "[Priority](#cfn-elasticloadbalancingv2-listenerrule-priority)" : Integer
    }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancingV2::ListenerRule
Properties : 
﻿  [Actions](#cfn-elasticloadbalancingv2-listenerrule-actions) : 
    - [Action](aws-properties-elasticloadbalancingv2-listenerrule-actions.md)
﻿  [Conditions](#cfn-elasticloadbalancingv2-listenerrule-conditions) : 
    - [RuleCondition](aws-properties-elasticloadbalancingv2-listenerrule-conditions.md)
﻿  [ListenerArn](#cfn-elasticloadbalancingv2-listenerrule-listenerarn) : String
﻿  [Priority](#cfn-elasticloadbalancingv2-listenerrule-priority) : Integer
```

## Properties<a name="aws-resource-elasticloadbalancingv2-listenerrule-properties"></a>

`Actions`  <a name="cfn-elasticloadbalancingv2-listenerrule-actions"></a>
The actions\.  
*Required*: Yes  
*Type*: List of [Action](aws-properties-elasticloadbalancingv2-listenerrule-actions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Conditions`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions"></a>
The conditions\.  
*Required*: Yes  
*Type*: List of [RuleCondition](aws-properties-elasticloadbalancingv2-listenerrule-conditions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ListenerArn`  <a name="cfn-elasticloadbalancingv2-listenerrule-listenerarn"></a>
The Amazon Resource Name \(ARN\) of the listener\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Priority`  <a name="cfn-elasticloadbalancingv2-listenerrule-priority"></a>
The rule priority\. A listener can't have multiple rules with the same priority\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-elasticloadbalancingv2-listenerrule-return-values"></a>

### Ref<a name="aws-resource-elasticloadbalancingv2-listenerrule-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the listener rule\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-elasticloadbalancingv2-listenerrule--seealso"></a>
+  [CreateRule](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateRule.html) in the *Elastic Load Balancing API Reference \(version 2015\-12\-01\)* 
+  [Listener Rules](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html#listener-rules) in the *User Guide for Application Load Balancers* 