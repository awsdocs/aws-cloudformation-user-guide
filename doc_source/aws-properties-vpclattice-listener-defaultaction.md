# AWS::VpcLattice::Listener DefaultAction<a name="aws-properties-vpclattice-listener-defaultaction"></a>

The action for the default rule\. Each listener has a default rule\. Each rule consists of a priority, one or more actions, and one or more conditions\. The default rule is the rule that's used if no other rules match\. Each rule must include exactly one of the following types of actions: `forward `or `fixed-response`, and it must be the last action to be performed\. 

## Syntax<a name="aws-properties-vpclattice-listener-defaultaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-listener-defaultaction-syntax.json"></a>

```
{
  "[FixedResponse](#cfn-vpclattice-listener-defaultaction-fixedresponse)" : FixedResponse,
  "[Forward](#cfn-vpclattice-listener-defaultaction-forward)" : Forward
}
```

### YAML<a name="aws-properties-vpclattice-listener-defaultaction-syntax.yaml"></a>

```
  [FixedResponse](#cfn-vpclattice-listener-defaultaction-fixedresponse): 
    FixedResponse
  [Forward](#cfn-vpclattice-listener-defaultaction-forward): 
    Forward
```

## Properties<a name="aws-properties-vpclattice-listener-defaultaction-properties"></a>

`FixedResponse`  <a name="cfn-vpclattice-listener-defaultaction-fixedresponse"></a>
Information about an action that returns a custom HTTP response\.   
*Required*: No  
*Type*: [FixedResponse](aws-properties-vpclattice-listener-fixedresponse.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Forward`  <a name="cfn-vpclattice-listener-defaultaction-forward"></a>
Describes a forward action\. You can use forward actions to route requests to one or more target groups\.   
*Required*: No  
*Type*: [Forward](aws-properties-vpclattice-listener-forward.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)