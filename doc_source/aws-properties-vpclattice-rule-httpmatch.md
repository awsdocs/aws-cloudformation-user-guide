# AWS::VpcLattice::Rule HttpMatch<a name="aws-properties-vpclattice-rule-httpmatch"></a>

Describes criteria that can be applied to incoming requests\.

## Syntax<a name="aws-properties-vpclattice-rule-httpmatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-httpmatch-syntax.json"></a>

```
{
  "[HeaderMatches](#cfn-vpclattice-rule-httpmatch-headermatches)" : [ HeaderMatch, ... ],
  "[Method](#cfn-vpclattice-rule-httpmatch-method)" : String,
  "[PathMatch](#cfn-vpclattice-rule-httpmatch-pathmatch)" : PathMatch
}
```

### YAML<a name="aws-properties-vpclattice-rule-httpmatch-syntax.yaml"></a>

```
  [HeaderMatches](#cfn-vpclattice-rule-httpmatch-headermatches): 
    - HeaderMatch
  [Method](#cfn-vpclattice-rule-httpmatch-method): String
  [PathMatch](#cfn-vpclattice-rule-httpmatch-pathmatch): 
    PathMatch
```

## Properties<a name="aws-properties-vpclattice-rule-httpmatch-properties"></a>

`HeaderMatches`  <a name="cfn-vpclattice-rule-httpmatch-headermatches"></a>
The header matches\. Matches incoming requests with rule based on request header value before applying rule action\.  
*Required*: No  
*Type*: List of [HeaderMatch](aws-properties-vpclattice-rule-headermatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Method`  <a name="cfn-vpclattice-rule-httpmatch-method"></a>
The HTTP method type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PathMatch`  <a name="cfn-vpclattice-rule-httpmatch-pathmatch"></a>
The path match\.  
*Required*: No  
*Type*: [PathMatch](aws-properties-vpclattice-rule-pathmatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)