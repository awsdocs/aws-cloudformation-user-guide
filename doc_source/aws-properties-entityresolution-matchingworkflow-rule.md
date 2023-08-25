# AWS::EntityResolution::MatchingWorkflow Rule<a name="aws-properties-entityresolution-matchingworkflow-rule"></a>

An object containing `RuleName`, and `MatchingKeys`\.

## Syntax<a name="aws-properties-entityresolution-matchingworkflow-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-entityresolution-matchingworkflow-rule-syntax.json"></a>

```
{
  "[MatchingKeys](#cfn-entityresolution-matchingworkflow-rule-matchingkeys)" : [ String, ... ],
  "[RuleName](#cfn-entityresolution-matchingworkflow-rule-rulename)" : String
}
```

### YAML<a name="aws-properties-entityresolution-matchingworkflow-rule-syntax.yaml"></a>

```
  [MatchingKeys](#cfn-entityresolution-matchingworkflow-rule-matchingkeys): 
    - String
  [RuleName](#cfn-entityresolution-matchingworkflow-rule-rulename): String
```

## Properties<a name="aws-properties-entityresolution-matchingworkflow-rule-properties"></a>

`MatchingKeys`  <a name="cfn-entityresolution-matchingworkflow-rule-matchingkeys"></a>
A list of `MatchingKeys`\. The `MatchingKeys` must have been defined in the `SchemaMapping`\. Two records are considered to match according to this rule if all of the `MatchingKeys` match\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleName`  <a name="cfn-entityresolution-matchingworkflow-rule-rulename"></a>
A name for the matching rule\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)