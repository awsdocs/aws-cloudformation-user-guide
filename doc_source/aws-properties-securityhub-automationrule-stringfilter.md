# AWS::SecurityHub::AutomationRule StringFilter<a name="aws-properties-securityhub-automationrule-stringfilter"></a>

A string filter for filtering AWS Security Hub findings\.

## Syntax<a name="aws-properties-securityhub-automationrule-stringfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-stringfilter-syntax.json"></a>

```
{
  "[Comparison](#cfn-securityhub-automationrule-stringfilter-comparison)" : String,
  "[Value](#cfn-securityhub-automationrule-stringfilter-value)" : String
}
```

### YAML<a name="aws-properties-securityhub-automationrule-stringfilter-syntax.yaml"></a>

```
  [Comparison](#cfn-securityhub-automationrule-stringfilter-comparison): String
  [Value](#cfn-securityhub-automationrule-stringfilter-value): String
```

## Properties<a name="aws-properties-securityhub-automationrule-stringfilter-properties"></a>

`Comparison`  <a name="cfn-securityhub-automationrule-stringfilter-comparison"></a>
The condition to apply to a string value when filtering Security Hub findings\.  
To search for values that have the filter value, use one of the following comparison operators:  
+ To search for values that include the filter value, use `CONTAINS`\. For example, the filter `Title CONTAINS CloudFront` matches findings that have a `Title` that includes the string CloudFront\.
+ To search for values that exactly match the filter value, use `EQUALS`\. For example, the filter `AwsAccountId EQUALS 123456789012` only matches findings that have an account ID of `123456789012`\.
+ To search for values that start with the filter value, use `PREFIX`\. For example, the filter `ResourceRegion PREFIX us` matches findings that have a `ResourceRegion` that starts with `us`\. A `ResourceRegion` that starts with a different value, such as `af`, `ap`, or `ca`, doesn't match\.
 `CONTAINS`, `EQUALS`, and `PREFIX` filters on the same field are joined by `OR`\. A finding matches if it matches any one of those filters\. For example, the filters `Title CONTAINS CloudFront OR Title CONTAINS CloudWatch` match a finding that includes either `CloudFront`, `CloudWatch`, or both strings in the title\.  
To search for values that don’t have the filter value, use one of the following comparison operators:  
+ To search for values that exclude the filter value, use `NOT_CONTAINS`\. For example, the filter `Title NOT_CONTAINS CloudFront` matches findings that have a `Title` that excludes the string CloudFront\.
+ To search for values other than the filter value, use `NOT_EQUALS`\. For example, the filter `AwsAccountId NOT_EQUALS 123456789012` only matches findings that have an account ID other than `123456789012`\.
+ To search for values that don't start with the filter value, use `PREFIX_NOT_EQUALS`\. For example, the filter `ResourceRegion PREFIX_NOT_EQUALS us` matches findings with a `ResourceRegion` that starts with a value other than `us`\.
 `NOT_CONTAINS`, `NOT_EQUALS`, and `PREFIX_NOT_EQUALS` filters on the same field are joined by `AND`\. A finding matches only if it matches all of those filters\. For example, the filters `Title NOT_CONTAINS CloudFront AND Title NOT_CONTAINS CloudWatch` match a finding that excludes both `CloudFront` and `CloudWatch` in the title\.  
You can’t have both a `CONTAINS` filter and a `NOT_CONTAINS` filter on the same field\. Similarly, you can't provide both an `EQUALS` filter and a `NOT_EQUALS` or `PREFIX_NOT_EQUALS` filter on the same field\. Combining filters in this way returns an error\. `CONTAINS` filters can only be used with other `CONTAINS` filters\. `NOT_CONTAINS` filters can only be used with other `NOT_CONTAINS` filters\.   
You can combine `PREFIX` filters with `NOT_EQUALS` or `PREFIX_NOT_EQUALS` filters for the same field\. Security Hub first processes the `PREFIX` filters, and then the `NOT_EQUALS` or `PREFIX_NOT_EQUALS` filters\.  
For example, for the following filters, Security Hub first identifies findings that have resource types that start with either `AwsIam` or `AwsEc2`\. It then excludes findings that have a resource type of `AwsIamPolicy` and findings that have a resource type of `AwsEc2NetworkInterface`\.  
+  `ResourceType PREFIX AwsIam` 
+  `ResourceType PREFIX AwsEc2` 
+  `ResourceType NOT_EQUALS AwsIamPolicy` 
+  `ResourceType NOT_EQUALS AwsEc2NetworkInterface` 
 `CONTAINS` and `NOT_CONTAINS` operators can be used only with automation rules\. For more information, see [Automation rules](https://docs.aws.amazon.com/securityhub/latest/userguide/automation-rules.html) in the * AWS Security Hub User Guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONTAINS | EQUALS | NOT_CONTAINS | NOT_EQUALS | PREFIX | PREFIX_NOT_EQUALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-securityhub-automationrule-stringfilter-value"></a>
The string filter value\. Filter values are case sensitive\. For example, the product name for control\-based findings is `Security Hub`\. If you provide `security hub` as the filter value, there's no match\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)