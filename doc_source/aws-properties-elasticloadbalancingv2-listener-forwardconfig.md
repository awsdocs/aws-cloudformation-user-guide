# AWS::ElasticLoadBalancingV2::Listener ForwardConfig<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig"></a>

Information for creating an action that distributes requests among one or more target groups\. For Network Load Balancers, you can specify a single target group\. Specify only when `Type` is `forward`\. If you specify both `ForwardConfig` and `TargetGroupArn`, you can specify only one target group using `ForwardConfig` and it must be the same target group specified in `TargetGroupArn`\.

## Syntax<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig-syntax.json"></a>

```
{
  "[TargetGroups](#cfn-elasticloadbalancingv2-listener-forwardconfig-targetgroups)" : [ TargetGroupTuple, ... ],
  "[TargetGroupStickinessConfig](#cfn-elasticloadbalancingv2-listener-forwardconfig-targetgroupstickinessconfig)" : TargetGroupStickinessConfig
}
```

### YAML<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig-syntax.yaml"></a>

```
  [TargetGroups](#cfn-elasticloadbalancingv2-listener-forwardconfig-targetgroups): 
    - TargetGroupTuple
  [TargetGroupStickinessConfig](#cfn-elasticloadbalancingv2-listener-forwardconfig-targetgroupstickinessconfig): 
    TargetGroupStickinessConfig
```

## Properties<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig-properties"></a>

`TargetGroups`  <a name="cfn-elasticloadbalancingv2-listener-forwardconfig-targetgroups"></a>
Information about how traffic will be distributed between multiple target groups in a forward rule\.  
*Required*: No  
*Type*: List of [TargetGroupTuple](aws-properties-elasticloadbalancingv2-listener-targetgrouptuple.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupStickinessConfig`  <a name="cfn-elasticloadbalancingv2-listener-forwardconfig-targetgroupstickinessconfig"></a>
Information about the target group stickiness for a rule\.  
*Required*: No  
*Type*: [TargetGroupStickinessConfig](aws-properties-elasticloadbalancingv2-listener-targetgroupstickinessconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig--examples"></a>



### Weighted Target Groups Example<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig--examples--Weighted_Target_Groups_Example"></a>

The following example sets the relative weight of traffic between two traffic groups\. Since the `weight` property of each group is set to the same value, `1`, traffic is split 50/50 between the two groups\.

#### JSON<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig--examples--Weighted_Target_Groups_Example--json"></a>

```
"ListenerRule1": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "ForwardConfig": {
            "TargetGroups": [{
              "TargetGroupArn": { "Ref": "TargetGroup1" },
              "Weight": 1
            }, {
              "TargetGroupArn": { "Ref": "TargetGroup2" },
              "Weight": 1
            }]
          }
        }],
        "Conditions": [{
          "Field": "path-pattern",
          "Values": ["foo"]
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 1
      }
    }
```

#### YAML<a name="aws-properties-elasticloadbalancingv2-listener-forwardconfig--examples--Weighted_Target_Groups_Example--yaml"></a>

```
ListenerRule1:
  Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
  Properties:
    Actions:
      - Type: forward
        ForwardConfig:
          TargetGroups:
            - TargetGroupArn: !Ref TargetGroup1
              Weight: 1
            - TargetGroupArn: !Ref TargetGroup2
              Weight: 1
    Conditions:
      - Field: path-pattern
        Values:
          - foo
    ListenerArn: !Ref Listener
    Priority: 1
```