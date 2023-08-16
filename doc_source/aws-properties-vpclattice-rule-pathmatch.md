# AWS::VpcLattice::Rule PathMatch<a name="aws-properties-vpclattice-rule-pathmatch"></a>

Describes the conditions that can be applied when matching a path for incoming requests\.

## Syntax<a name="aws-properties-vpclattice-rule-pathmatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-pathmatch-syntax.json"></a>

```
{
  "[CaseSensitive](#cfn-vpclattice-rule-pathmatch-casesensitive)" : Boolean,
  "[Match](#cfn-vpclattice-rule-pathmatch-match)" : PathMatchType
}
```

### YAML<a name="aws-properties-vpclattice-rule-pathmatch-syntax.yaml"></a>

```
  [CaseSensitive](#cfn-vpclattice-rule-pathmatch-casesensitive): Boolean
  [Match](#cfn-vpclattice-rule-pathmatch-match): 
    PathMatchType
```

## Properties<a name="aws-properties-vpclattice-rule-pathmatch-properties"></a>

`CaseSensitive`  <a name="cfn-vpclattice-rule-pathmatch-casesensitive"></a>
Indicates whether the match is case sensitive\. Defaults to false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-vpclattice-rule-pathmatch-match"></a>
The type of path match\.  
*Required*: Yes  
*Type*: [PathMatchType](aws-properties-vpclattice-rule-pathmatchtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)