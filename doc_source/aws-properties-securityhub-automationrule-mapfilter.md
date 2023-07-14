# AWS::SecurityHub::AutomationRule MapFilter<a name="aws-properties-securityhub-automationrule-mapfilter"></a>

A map filter for querying findings\. Each map filter provides the field to check, the value to look for, and the comparison operator\.

## Syntax<a name="aws-properties-securityhub-automationrule-mapfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-mapfilter-syntax.json"></a>

```
{
  "[Comparison](#cfn-securityhub-automationrule-mapfilter-comparison)" : String,
  "[Key](#cfn-securityhub-automationrule-mapfilter-key)" : String,
  "[Value](#cfn-securityhub-automationrule-mapfilter-value)" : String
}
```

### YAML<a name="aws-properties-securityhub-automationrule-mapfilter-syntax.yaml"></a>

```
  [Comparison](#cfn-securityhub-automationrule-mapfilter-comparison): String
  [Key](#cfn-securityhub-automationrule-mapfilter-key): String
  [Value](#cfn-securityhub-automationrule-mapfilter-value): String
```

## Properties<a name="aws-properties-securityhub-automationrule-mapfilter-properties"></a>

`Comparison`  <a name="cfn-securityhub-automationrule-mapfilter-comparison"></a>
The condition to apply to the key value when querying for findings with a map filter\.  
To search for values that exactly match the filter value, use `EQUALS`\. For example, for the `ResourceTags` field, the filter `Department EQUALS Security` matches findings that have the value `Security` for the tag `Department`\.  
To search for values other than the filter value, use `NOT_EQUALS`\. For example, for the `ResourceTags` field, the filter `Department NOT_EQUALS Finance` matches findings that do not have the value `Finance` for the tag `Department`\.  
 `EQUALS` filters on the same field are joined by `OR`\. A finding matches if it matches any one of those filters\.  
 `NOT_EQUALS` filters on the same field are joined by `AND`\. A finding matches only if it matches all of those filters\.  
You cannot have both an `EQUALS` filter and a `NOT_EQUALS` filter on the same field\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EQUALS | NOT_EQUALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-securityhub-automationrule-mapfilter-key"></a>
The key of the map filter\. For example, for `ResourceTags`, `Key` identifies the name of the tag\. For `UserDefinedFields`, `Key` is the name of the field\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-securityhub-automationrule-mapfilter-value"></a>
The value for the key in the map filter\. Filter values are case sensitive\. For example, one of the values for a tag called `Department` might be `Security`\. If you provide `security` as the filter value, then there is no match\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)