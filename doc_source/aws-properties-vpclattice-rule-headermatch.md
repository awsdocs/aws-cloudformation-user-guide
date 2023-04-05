# AWS::VpcLattice::Rule HeaderMatch<a name="aws-properties-vpclattice-rule-headermatch"></a>

Describes the constraints for a header match\. Matches incoming requests with rule based on request header value before applying rule action\.

## Syntax<a name="aws-properties-vpclattice-rule-headermatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-headermatch-syntax.json"></a>

```
{
  "[CaseSensitive](#cfn-vpclattice-rule-headermatch-casesensitive)" : Boolean,
  "[Match](#cfn-vpclattice-rule-headermatch-match)" : HeaderMatchType,
  "[Name](#cfn-vpclattice-rule-headermatch-name)" : String
}
```

### YAML<a name="aws-properties-vpclattice-rule-headermatch-syntax.yaml"></a>

```
  [CaseSensitive](#cfn-vpclattice-rule-headermatch-casesensitive): Boolean
  [Match](#cfn-vpclattice-rule-headermatch-match): 
    HeaderMatchType
  [Name](#cfn-vpclattice-rule-headermatch-name): String
```

## Properties<a name="aws-properties-vpclattice-rule-headermatch-properties"></a>

`CaseSensitive`  <a name="cfn-vpclattice-rule-headermatch-casesensitive"></a>
Indicates whether the match is case sensitive\. Defaults to false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-vpclattice-rule-headermatch-match"></a>
The header match type\.  
*Required*: Yes  
*Type*: [HeaderMatchType](aws-properties-vpclattice-rule-headermatchtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-vpclattice-rule-headermatch-name"></a>
The name of the header\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)