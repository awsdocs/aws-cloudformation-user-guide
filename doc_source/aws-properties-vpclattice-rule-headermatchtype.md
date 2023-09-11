# AWS::VpcLattice::Rule HeaderMatchType<a name="aws-properties-vpclattice-rule-headermatchtype"></a>

Describes a header match type\.

## Syntax<a name="aws-properties-vpclattice-rule-headermatchtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-headermatchtype-syntax.json"></a>

```
{
  "[Contains](#cfn-vpclattice-rule-headermatchtype-contains)" : String,
  "[Exact](#cfn-vpclattice-rule-headermatchtype-exact)" : String,
  "[Prefix](#cfn-vpclattice-rule-headermatchtype-prefix)" : String
}
```

### YAML<a name="aws-properties-vpclattice-rule-headermatchtype-syntax.yaml"></a>

```
  [Contains](#cfn-vpclattice-rule-headermatchtype-contains): String
  [Exact](#cfn-vpclattice-rule-headermatchtype-exact): String
  [Prefix](#cfn-vpclattice-rule-headermatchtype-prefix): String
```

## Properties<a name="aws-properties-vpclattice-rule-headermatchtype-properties"></a>

`Contains`  <a name="cfn-vpclattice-rule-headermatchtype-contains"></a>
A contains type match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Exact`  <a name="cfn-vpclattice-rule-headermatchtype-exact"></a>
An exact type match\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-vpclattice-rule-headermatchtype-prefix"></a>
A prefix type match\. Matches the value with the prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)