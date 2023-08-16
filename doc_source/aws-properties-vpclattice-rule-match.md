# AWS::VpcLattice::Rule Match<a name="aws-properties-vpclattice-rule-match"></a>

Describes a rule match\.

## Syntax<a name="aws-properties-vpclattice-rule-match-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-match-syntax.json"></a>

```
{
  "[HttpMatch](#cfn-vpclattice-rule-match-httpmatch)" : HttpMatch
}
```

### YAML<a name="aws-properties-vpclattice-rule-match-syntax.yaml"></a>

```
  [HttpMatch](#cfn-vpclattice-rule-match-httpmatch): 
    HttpMatch
```

## Properties<a name="aws-properties-vpclattice-rule-match-properties"></a>

`HttpMatch`  <a name="cfn-vpclattice-rule-match-httpmatch"></a>
The HTTP criteria that a rule must match\.  
*Required*: Yes  
*Type*: [HttpMatch](aws-properties-vpclattice-rule-httpmatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)