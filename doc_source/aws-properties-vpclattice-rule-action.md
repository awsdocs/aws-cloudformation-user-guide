# AWS::VpcLattice::Rule Action<a name="aws-properties-vpclattice-rule-action"></a>

Describes the action for a rule\. Each rule must include exactly one of the following types of actions: `forward` or `fixed-response`, and it must be the last action to be performed\.

## Syntax<a name="aws-properties-vpclattice-rule-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-action-syntax.json"></a>

```
{
  "[FixedResponse](#cfn-vpclattice-rule-action-fixedresponse)" : FixedResponse,
  "[Forward](#cfn-vpclattice-rule-action-forward)" : Forward
}
```

### YAML<a name="aws-properties-vpclattice-rule-action-syntax.yaml"></a>

```
  [FixedResponse](#cfn-vpclattice-rule-action-fixedresponse): 
    FixedResponse
  [Forward](#cfn-vpclattice-rule-action-forward): 
    Forward
```

## Properties<a name="aws-properties-vpclattice-rule-action-properties"></a>

`FixedResponse`  <a name="cfn-vpclattice-rule-action-fixedresponse"></a>
Describes the rule action that returns a custom HTTP response\.  
*Required*: No  
*Type*: [FixedResponse](aws-properties-vpclattice-rule-fixedresponse.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Forward`  <a name="cfn-vpclattice-rule-action-forward"></a>
The forward action\. Traffic that matches the rule is forwarded to the specified target groups\.  
*Required*: No  
*Type*: [Forward](aws-properties-vpclattice-rule-forward.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)