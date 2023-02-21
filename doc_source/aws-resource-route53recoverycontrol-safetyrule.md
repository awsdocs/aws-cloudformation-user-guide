# AWS::Route53RecoveryControl::SafetyRule<a name="aws-resource-route53recoverycontrol-safetyrule"></a>

List the safety rules \(the assertion rules and gating rules\) that you've defined for the routing controls in a control panel\. 

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
      "[RuleConfig](#cfn-route53recoverycontrol-safetyrule-ruleconfig)" : RuleConfig,
      "[Tags](#cfn-route53recoverycontrol-safetyrule-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
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
  [Tags](#cfn-route53recoverycontrol-safetyrule-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53recoverycontrol-safetyrule-properties"></a>

`AssertionRule`  <a name="cfn-route53recoverycontrol-safetyrule-assertionrule"></a>
An assertion rule enforces that, when you change a routing control state, that the criteria that you set in the rule configuration is met\. Otherwise, the change to the routing control is not accepted\. For example, the criteria might be that at least one routing control state is `On` after the transaction so that traffic continues to flow to at least one cell for the application\. This ensures that you avoid a fail\-open scenario\.  
*Required*: No  
*Type*: [AssertionRule](aws-properties-route53recoverycontrol-safetyrule-assertionrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ControlPanelArn`  <a name="cfn-route53recoverycontrol-safetyrule-controlpanelarn"></a>
The Amazon Resource Name \(ARN\) for the control panel\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GatingRule`  <a name="cfn-route53recoverycontrol-safetyrule-gatingrule"></a>
A gating rule verifies that a gating routing control or set of gating routing controls, evaluates as true, based on a rule configuration that you specify, which allows a set of routing control state changes to complete\.  
For example, if you specify one gating routing control and you set the `Type` in the rule configuration to `OR`, that indicates that you must set the gating routing control to `On` for the rule to evaluate as true; that is, for the gating control "switch" to be "On"\. When you do that, then you can update the routing control states for the target routing controls that you specify in the gating rule\.  
*Required*: No  
*Type*: [GatingRule](aws-properties-route53recoverycontrol-safetyrule-gatingrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53recoverycontrol-safetyrule-name"></a>
The name of the assertion rule\. The name must be unique within a control panel\. You can use any non\-white space character in the name except the following: & > < ' \(single quote\) " \(double quote\) ; \(semicolon\)  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleConfig`  <a name="cfn-route53recoverycontrol-safetyrule-ruleconfig"></a>
The criteria that you set for specific assertion controls \(routing controls\) that designate how many control states must be `ON` as the result of a transaction\. For example, if you have three assertion controls, you might specify `ATLEAST 2` for your rule configuration\. This means that at least two assertion controls must be `ON`, so that at least two AWS Regions have traffic flowing to them\.   
*Required*: Yes  
*Type*: [RuleConfig](aws-properties-route53recoverycontrol-safetyrule-ruleconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-route53recoverycontrol-safetyrule-tags"></a>
The value for a tag\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
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
The deployment status of the safety rule\. Status can be one of the following: PENDING, DEPLOYED, PENDING\_DELETION\.