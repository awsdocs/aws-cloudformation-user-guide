# AWS::VpcLattice::Rule WeightedTargetGroup<a name="aws-properties-vpclattice-rule-weightedtargetgroup"></a>

Describes the weight of a target group\.

## Syntax<a name="aws-properties-vpclattice-rule-weightedtargetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-weightedtargetgroup-syntax.json"></a>

```
{
  "[TargetGroupIdentifier](#cfn-vpclattice-rule-weightedtargetgroup-targetgroupidentifier)" : String,
  "[Weight](#cfn-vpclattice-rule-weightedtargetgroup-weight)" : Integer
}
```

### YAML<a name="aws-properties-vpclattice-rule-weightedtargetgroup-syntax.yaml"></a>

```
  [TargetGroupIdentifier](#cfn-vpclattice-rule-weightedtargetgroup-targetgroupidentifier): String
  [Weight](#cfn-vpclattice-rule-weightedtargetgroup-weight): Integer
```

## Properties<a name="aws-properties-vpclattice-rule-weightedtargetgroup-properties"></a>

`TargetGroupIdentifier`  <a name="cfn-vpclattice-rule-weightedtargetgroup-targetgroupidentifier"></a>
The ID of the target group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-vpclattice-rule-weightedtargetgroup-weight"></a>
Only required if you specify multiple target groups for a forward action\. The "weight" determines how requests are distributed to the target group\. For example, if you specify two target groups, each with a weight of 10, each target group receives half the requests\. If you specify two target groups, one with a weight of 10 and the other with a weight of 20, the target group with a weight of 20 receives twice as many requests as the other target group\. If there's only one target group specified, then the default value is 100\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)