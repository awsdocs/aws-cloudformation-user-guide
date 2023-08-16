# AWS::SecurityHub::AutomationRule MapFilter<a name="aws-properties-securityhub-automationrule-mapfilter"></a>

A map filter for filtering AWS Security Hub findings\. Each map filter provides the field to check for, the value to check for, and the comparison operator\.

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
The condition to apply to the key value when filtering Security Hub findings with a map filter\.  
To search for values that have the filter value, use one of the following comparison operators:  
+ To search for values that include the filter value, use `CONTAINS`\. For example, for the `ResourceTags` field, the filter `Department CONTAINS Security` matches findings that include the value `Security` for the `Department` tag\. In the same example, a finding with a value of `Security team` for the `Department` tag is a match\.
+ To search for values that exactly match the filter value, use `EQUALS`\. For example, for the `ResourceTags` field, the filter `Department EQUALS Security` matches findings that have the value `Security` for the `Department` tag\.
 `CONTAINS` and `EQUALS` filters on the same field are joined by `OR`\. A finding matches if it matches any one of those filters\. For example, the filters `Department CONTAINS Security OR Department CONTAINS Finance` match a finding that includes either `Security`, `Finance`, or both values\.  
To search for values that don't have the filter value, use one of the following comparison operators:  
+ To search for values that exclude the filter value, use `NOT_CONTAINS`\. For example, for the `ResourceTags` field, the filter `Department NOT_CONTAINS Finance` matches findings that exclude the value `Finance` for the `Department` tag\.
+ To search for values other than the filter value, use `NOT_EQUALS`\. For example, for the `ResourceTags` field, the filter `Department NOT_EQUALS Finance` matches findings that don’t have the value `Finance` for the `Department` tag\.
 `NOT_CONTAINS` and `NOT_EQUALS` filters on the same field are joined by `AND`\. A finding matches only if it matches all of those filters\. For example, the filters `Department NOT_CONTAINS Security AND Department NOT_CONTAINS Finance` match a finding that excludes both the `Security` and `Finance` values\.  
 `CONTAINS` filters can only be used with other `CONTAINS` filters\. `NOT_CONTAINS` filters can only be used with other `NOT_CONTAINS` filters\.  
You can’t have both a `CONTAINS` filter and a `NOT_CONTAINS` filter on the same field\. Similarly, you can’t have both an `EQUALS` filter and a `NOT_EQUALS` filter on the same field\. Combining filters in this way returns an error\.   
 `CONTAINS` and `NOT_CONTAINS` operators can be used only with automation rules\. For more information, see [Automation rules](https://docs.aws.amazon.com/securityhub/latest/userguide/automation-rules.html) in the * AWS Security Hub User Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTAINS | EQUALS | NOT_CONTAINS | NOT_EQUALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-securityhub-automationrule-mapfilter-key"></a>
The key of the map filter\. For example, for `ResourceTags`, `Key` identifies the name of the tag\. For `UserDefinedFields`, `Key` is the name of the field\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-securityhub-automationrule-mapfilter-value"></a>
The value for the key in the map filter\. Filter values are case sensitive\. For example, one of the values for a tag called `Department` might be `Security`\. If you provide `security` as the filter value, then there's no match\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)