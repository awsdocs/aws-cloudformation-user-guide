# AWS::SecurityHub::AutomationRule DateFilter<a name="aws-properties-securityhub-automationrule-datefilter"></a>

A date filter for querying findings\.

## Syntax<a name="aws-properties-securityhub-automationrule-datefilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-datefilter-syntax.json"></a>

```
{
  "[DateRange](#cfn-securityhub-automationrule-datefilter-daterange)" : DateRange,
  "[End](#cfn-securityhub-automationrule-datefilter-end)" : String,
  "[Start](#cfn-securityhub-automationrule-datefilter-start)" : String
}
```

### YAML<a name="aws-properties-securityhub-automationrule-datefilter-syntax.yaml"></a>

```
  [DateRange](#cfn-securityhub-automationrule-datefilter-daterange): 
    DateRange
  [End](#cfn-securityhub-automationrule-datefilter-end): String
  [Start](#cfn-securityhub-automationrule-datefilter-start): String
```

## Properties<a name="aws-properties-securityhub-automationrule-datefilter-properties"></a>

`DateRange`  <a name="cfn-securityhub-automationrule-datefilter-daterange"></a>
A date range for the date filter\.  
*Required*: No  
*Type*: [DateRange](aws-properties-securityhub-automationrule-daterange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`End`  <a name="cfn-securityhub-automationrule-datefilter-end"></a>
A timestamp that provides the end date for the date filter\.  
A correctly formatted example is `2020-05-21T20:16:34.724Z`\. The value cannot contain spaces, and date and time should be separated by `T`\. For more information, see [RFC 3339 section 5\.6, Internet Date/Time Format](https://www.rfc-editor.org/rfc/rfc3339#section-5.6)\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Start`  <a name="cfn-securityhub-automationrule-datefilter-start"></a>
A timestamp that provides the start date for the date filter\.  
A correctly formatted example is `2020-05-21T20:16:34.724Z`\. The value cannot contain spaces, and date and time should be separated by `T`\. For more information, see [RFC 3339 section 5\.6, Internet Date/Time Format](https://www.rfc-editor.org/rfc/rfc3339#section-5.6)\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)