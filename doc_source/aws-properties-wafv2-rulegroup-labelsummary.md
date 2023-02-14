# AWS::WAFv2::RuleGroup LabelSummary<a name="aws-properties-wafv2-rulegroup-labelsummary"></a>

List of labels used by one or more of the rules of a [AWS::WAFv2::RuleGroup](aws-resource-wafv2-rulegroup.md)\. This summary object is used for the following rule group lists: 
+  `AvailableLabels` \- Labels that rules add to matching requests\. These labels are defined in the `RuleLabels` for a `Rule`\. 
+  `ConsumedLabels` \- Labels that rules match against\. These labels are defined in a `LabelMatchStatement` specification, in the rule statement\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-labelsummary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-labelsummary-syntax.json"></a>

```
{
  "[Name](#cfn-wafv2-rulegroup-labelsummary-name)" : String
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-labelsummary-syntax.yaml"></a>

```
  [Name](#cfn-wafv2-rulegroup-labelsummary-name): String
```

## Properties<a name="aws-properties-wafv2-rulegroup-labelsummary-properties"></a>

`Name`  <a name="cfn-wafv2-rulegroup-labelsummary-name"></a>
An individual label specification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)