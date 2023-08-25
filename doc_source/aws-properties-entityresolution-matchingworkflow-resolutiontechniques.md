# AWS::EntityResolution::MatchingWorkflow ResolutionTechniques<a name="aws-properties-entityresolution-matchingworkflow-resolutiontechniques"></a>

An object which defines the `resolutionType` and the `ruleBasedProperties`

## Syntax<a name="aws-properties-entityresolution-matchingworkflow-resolutiontechniques-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-entityresolution-matchingworkflow-resolutiontechniques-syntax.json"></a>

```
{
  "[ResolutionType](#cfn-entityresolution-matchingworkflow-resolutiontechniques-resolutiontype)" : String,
  "[RuleBasedProperties](#cfn-entityresolution-matchingworkflow-resolutiontechniques-rulebasedproperties)" : RuleBasedProperties
}
```

### YAML<a name="aws-properties-entityresolution-matchingworkflow-resolutiontechniques-syntax.yaml"></a>

```
  [ResolutionType](#cfn-entityresolution-matchingworkflow-resolutiontechniques-resolutiontype): String
  [RuleBasedProperties](#cfn-entityresolution-matchingworkflow-resolutiontechniques-rulebasedproperties): 
    RuleBasedProperties
```

## Properties<a name="aws-properties-entityresolution-matchingworkflow-resolutiontechniques-properties"></a>

`ResolutionType`  <a name="cfn-entityresolution-matchingworkflow-resolutiontechniques-resolutiontype"></a>
There are two types of matching, `RULE_MATCHING` and `ML_MATCHING`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleBasedProperties`  <a name="cfn-entityresolution-matchingworkflow-resolutiontechniques-rulebasedproperties"></a>
An object which defines the list of matching rules to run and has a field `Rules`, which is a list of rule objects\.  
*Required*: No  
*Type*: [RuleBasedProperties](aws-properties-entityresolution-matchingworkflow-rulebasedproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)