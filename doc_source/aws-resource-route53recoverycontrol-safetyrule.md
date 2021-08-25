# AWS::Route53RecoveryControl::SafetyRule<a name="aws-resource-route53recoverycontrol-safetyrule"></a>

Defines the safety rules \(the assertion rules and gating rulest\) for the routing controls in a control panel\. 

## Syntax<a name="aws-resource-route53recoverycontrol-safetyrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53recoverycontrol-safetyrule-syntax.json"></a>

```
{
  "Type" : "AWS::Route53RecoveryControl::SafetyRule",
  "Properties" : {
      "[AssertionRule](#cfn-route53recoverycontrol-safetyrule-assertionrule)" : AssertionRule,
      "[ControlPanelArn](#cfn-route53recoverycontrol-safetyrule-controlpanelarn)" : String,
      "[GatingRule](#cfn-route53recoverycontrol-safetyrule-gatingrule)" : GatingRule,
      "[Name](#cfn-route53recoverycontrol-safetyrule-name)" : String,
      "[RuleConfig](#cfn-route53recoverycontrol-safetyrule-ruleconfig)" : RuleConfig
    }
}
```

### YAML<a name="aws-resource-route53recoverycontrol-safetyrule-syntax.yaml"></a>

```
Type: AWS::Route53RecoveryControl::SafetyRule
Properties: 
  [AssertionRule](#cfn-route53recoverycontrol-safetyrule-assertionrule): 
    AssertionRule
  [ControlPanelArn](#cfn-route53recoverycontrol-safetyrule-controlpanelarn): String
  [GatingRule](#cfn-route53recoverycontrol-safetyrule-gatingrule): 
    GatingRule
  [Name](#cfn-route53recoverycontrol-safetyrule-name): String
  [RuleConfig](#cfn-route53recoverycontrol-safetyrule-ruleconfig): 
    RuleConfig
```

## Properties<a name="aws-resource-route53recoverycontrol-safetyrule-properties"></a>

`AssertionRule`  <a name="cfn-route53recoverycontrol-safetyrule-assertionrule"></a>
An assertion rule enforces that, when a routing control state is changed, that the criteria set by the rule configuration is met\. Otherwise, the change to the routing control is not accepted\.  
*Required*: No  
*Type*: [AssertionRule](aws-properties-route53recoverycontrol-safetyrule-assertionrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ControlPanelArn`  <a name="cfn-route53recoverycontrol-safetyrule-controlpanelarn"></a>
The Amazon Resource Name \(ARN\) for the control panel\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GatingRule`  <a name="cfn-route53recoverycontrol-safetyrule-gatingrule"></a>
A gating rule verifies that a set of gating controls evaluates as true, based on a rule configuration that you specify\. If the gating rule evaluates to true, Amazon Route 53 Application Recovery Controller allows a set of routing control state changes to run and complete against the set of target controls\.  
*Required*: No  
*Type*: [GatingRule](aws-properties-route53recoverycontrol-safetyrule-gatingrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53recoverycontrol-safetyrule-name"></a>
The name of the assertion rule\. You can use any non\-white space character in the name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RuleConfig`  <a name="cfn-route53recoverycontrol-safetyrule-ruleconfig"></a>
The criteria that you set for specific assertion controls \(routing controls\) that designate how many controls must be enabled as the result of a transaction\. For example, if you have three assertion controls, you might specify `atleast` 2 for your rule configuration\. This means that at least two assertion controls must be enabled, so that at least two AWS Regions are enabled\.   
*Required*: Yes  
*Type*: [RuleConfig](aws-properties-route53recoverycontrol-safetyrule-ruleconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53recoverycontrol-safetyrule-return-values"></a>

### Ref<a name="aws-resource-route53recoverycontrol-safetyrule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `SafetyRuleArn` object\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53recoverycontrol-safetyrule-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53recoverycontrol-safetyrule-return-values-fn--getatt-fn--getatt"></a>

`SafetyRuleArn`  <a name="SafetyRuleArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the safety rule\.

`Status`  <a name="Status-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.