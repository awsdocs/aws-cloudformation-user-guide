# AWS::Route53RecoveryControl::SafetyRule GatingRule<a name="aws-properties-route53recoverycontrol-safetyrule-gatingrule"></a>

A gating rule verifies that a set of gating controls evaluates as true, based on a rule configuration that you specify\. If the gating rule evaluates to true, Amazon Route 53 Application Recovery Controller allows a set of routing control state changes to run and complete against the set of target controls\.

## Syntax<a name="aws-properties-route53recoverycontrol-safetyrule-gatingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53recoverycontrol-safetyrule-gatingrule-syntax.json"></a>

```
{
  "[GatingControls](#cfn-route53recoverycontrol-safetyrule-gatingrule-gatingcontrols)" : [ String, ... ],
  "[TargetControls](#cfn-route53recoverycontrol-safetyrule-gatingrule-targetcontrols)" : [ String, ... ],
  "[WaitPeriodMs](#cfn-route53recoverycontrol-safetyrule-gatingrule-waitperiodms)" : Integer
}
```

### YAML<a name="aws-properties-route53recoverycontrol-safetyrule-gatingrule-syntax.yaml"></a>

```
  [GatingControls](#cfn-route53recoverycontrol-safetyrule-gatingrule-gatingcontrols): 
    - String
  [TargetControls](#cfn-route53recoverycontrol-safetyrule-gatingrule-targetcontrols): 
    - String
  [WaitPeriodMs](#cfn-route53recoverycontrol-safetyrule-gatingrule-waitperiodms): Integer
```

## Properties<a name="aws-properties-route53recoverycontrol-safetyrule-gatingrule-properties"></a>

`GatingControls`  <a name="cfn-route53recoverycontrol-safetyrule-gatingrule-gatingcontrols"></a>
The gating controls for the gating rule\. That is, routing controls that are evaluated by the rule configuration that you specify\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetControls`  <a name="cfn-route53recoverycontrol-safetyrule-gatingrule-targetcontrols"></a>
Routing controls that can only be set or unset if the specified `RuleConfig` evaluates to true for the specified `GatingControls`\. For example, say you have three gating controls, one for each of three AWS Regions\. Now you specify `AtLeast 2` as your `RuleConfig`\. With these settings, you can only change \(set or unset\) the routing controls that you have specified as `TargetControls` if that rule evaluates to true\.   
In other words, your ability to change the routing controls that you have specified as `TargetControls` is gated by the rule that you set for the routing controls in `GatingControls`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitPeriodMs`  <a name="cfn-route53recoverycontrol-safetyrule-gatingrule-waitperiodms"></a>
An evaluation period, in milliseconds \(ms\), during which any request against the target routing controls will fail\. This helps prevent "flapping" of state\. The wait period is 5000 ms by default, but you can choose a custom value\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)