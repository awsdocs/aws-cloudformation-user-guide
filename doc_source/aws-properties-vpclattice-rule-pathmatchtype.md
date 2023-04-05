# AWS::VpcLattice::Rule PathMatchType<a name="aws-properties-vpclattice-rule-pathmatchtype"></a>

Describes a path match type\. Each rule can include only one of the following types of paths\.

## Syntax<a name="aws-properties-vpclattice-rule-pathmatchtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-pathmatchtype-syntax.json"></a>

```
{
  "[Exact](#cfn-vpclattice-rule-pathmatchtype-exact)" : String,
  "[Prefix](#cfn-vpclattice-rule-pathmatchtype-prefix)" : String
}
```

### YAML<a name="aws-properties-vpclattice-rule-pathmatchtype-syntax.yaml"></a>

```
  [Exact](#cfn-vpclattice-rule-pathmatchtype-exact): String
  [Prefix](#cfn-vpclattice-rule-pathmatchtype-prefix): String
```

## Properties<a name="aws-properties-vpclattice-rule-pathmatchtype-properties"></a>

`Exact`  <a name="cfn-vpclattice-rule-pathmatchtype-exact"></a>
An exact match of the path\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-vpclattice-rule-pathmatchtype-prefix"></a>
A prefix match of the path\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)