# AWS::VpcLattice::Rule Forward<a name="aws-properties-vpclattice-rule-forward"></a>

The forward action\. Traffic that matches the rule is forwarded to the specified target groups\.

## Syntax<a name="aws-properties-vpclattice-rule-forward-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-forward-syntax.json"></a>

```
{
  "[TargetGroups](#cfn-vpclattice-rule-forward-targetgroups)" : [ WeightedTargetGroup, ... ]
}
```

### YAML<a name="aws-properties-vpclattice-rule-forward-syntax.yaml"></a>

```
  [TargetGroups](#cfn-vpclattice-rule-forward-targetgroups): 
    - WeightedTargetGroup
```

## Properties<a name="aws-properties-vpclattice-rule-forward-properties"></a>

`TargetGroups`  <a name="cfn-vpclattice-rule-forward-targetgroups"></a>
The target groups\. Traffic matching the rule is forwarded to the specified target groups\. With forward actions, you can assign a weight that controls the prioritization and selection of each target group\. This means that requests are distributed to individual target groups based on their weights\. For example, if two target groups have the same weight, each target group receives half of the traffic\.  
The default value is 1\. This means that if only one target group is provided, there is no need to set the weight; 100% of traffic will go to that target group\.  
*Required*: Yes  
*Type*: List of [WeightedTargetGroup](aws-properties-vpclattice-rule-weightedtargetgroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)