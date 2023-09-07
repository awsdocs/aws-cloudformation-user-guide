# AWS::EntityResolution::MatchingWorkflow RuleBasedProperties<a name="aws-properties-entityresolution-matchingworkflow-rulebasedproperties"></a>

An object which defines the list of matching rules to run and has a field `Rules`, which is a list of rule objects\.

## Syntax<a name="aws-properties-entityresolution-matchingworkflow-rulebasedproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-entityresolution-matchingworkflow-rulebasedproperties-syntax.json"></a>

```
{
  "[AttributeMatchingModel](#cfn-entityresolution-matchingworkflow-rulebasedproperties-attributematchingmodel)" : String,
  "[Rules](#cfn-entityresolution-matchingworkflow-rulebasedproperties-rules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-entityresolution-matchingworkflow-rulebasedproperties-syntax.yaml"></a>

```
  [AttributeMatchingModel](#cfn-entityresolution-matchingworkflow-rulebasedproperties-attributematchingmodel): String
  [Rules](#cfn-entityresolution-matchingworkflow-rulebasedproperties-rules): 
    - Rule
```

## Properties<a name="aws-properties-entityresolution-matchingworkflow-rulebasedproperties-properties"></a>

`AttributeMatchingModel`  <a name="cfn-entityresolution-matchingworkflow-rulebasedproperties-attributematchingmodel"></a>
The comparison type\. You can either choose `ONE_TO_ONE` or `MANY_TO_MANY` as the AttributeMatchingModel\. When choosing `MANY_TO_MANY`, the system can match attributes across the sub\-types of an attribute type\. For example, if the value of the `Email` field of Profile A and the value of `BusinessEmail` field of Profile B matches, the two profiles are matched on the `Email` type\. When choosing `ONE_TO_ONE` ,the system can only match if the sub\-types are exact matches\. For example, only when the value of the `Email` field of Profile A and the value of the `Email` field of Profile B matches, the two profiles are matched on the `Email` type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Rules`  <a name="cfn-entityresolution-matchingworkflow-rulebasedproperties-rules"></a>
A list of `Rule` objects, each of which have fields `RuleName` and `MatchingKeys`\.  
*Required*: Yes  
*Type*: List of [Rule](aws-properties-entityresolution-matchingworkflow-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)