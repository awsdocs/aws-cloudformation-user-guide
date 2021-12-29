# AWS::Route53RecoveryControl::SafetyRule AssertionRule<a name="aws-properties-route53recoverycontrol-safetyrule-assertionrule"></a>

An assertion rule enforces that, when you change a routing control state, that the criteria that you set in the rule configuration is met\. Otherwise, the change to the routing control is not accepted\. For example, the criteria might be that at least one routing control state is `On` after the transaction so that traffic continues to flow to at least one cell for the application\. This ensures that you avoid a fail\-open scenario\.

## Syntax<a name="aws-properties-route53recoverycontrol-safetyrule-assertionrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53recoverycontrol-safetyrule-assertionrule-syntax.json"></a>

```
{
  "[AssertedControls](#cfn-route53recoverycontrol-safetyrule-assertionrule-assertedcontrols)" : [ String, ... ],
  "[WaitPeriodMs](#cfn-route53recoverycontrol-safetyrule-assertionrule-waitperiodms)" : Integer
}
```

### YAML<a name="aws-properties-route53recoverycontrol-safetyrule-assertionrule-syntax.yaml"></a>

```
  [AssertedControls](#cfn-route53recoverycontrol-safetyrule-assertionrule-assertedcontrols): 
    - String
  [WaitPeriodMs](#cfn-route53recoverycontrol-safetyrule-assertionrule-waitperiodms): Integer
```

## Properties<a name="aws-properties-route53recoverycontrol-safetyrule-assertionrule-properties"></a>

`AssertedControls`  <a name="cfn-route53recoverycontrol-safetyrule-assertionrule-assertedcontrols"></a>
The routing controls that are part of transactions that are evaluated to determine if a request to change a routing control state is allowed\. For example, you might include three routing controls, one for each of three AWS Regions\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WaitPeriodMs`  <a name="cfn-route53recoverycontrol-safetyrule-assertionrule-waitperiodms"></a>
An evaluation period, in milliseconds \(ms\), during which any request against the target routing controls will fail\. This helps prevent "flapping" of state\. The wait period is 5000 ms by default, but you can choose a custom value\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)