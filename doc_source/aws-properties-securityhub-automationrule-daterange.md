# AWS::SecurityHub::AutomationRule DateRange<a name="aws-properties-securityhub-automationrule-daterange"></a>

A date range for the date filter\.

## Syntax<a name="aws-properties-securityhub-automationrule-daterange-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-daterange-syntax.json"></a>

```
{
  "[Unit](#cfn-securityhub-automationrule-daterange-unit)" : String,
  "[Value](#cfn-securityhub-automationrule-daterange-value)" : Double
}
```

### YAML<a name="aws-properties-securityhub-automationrule-daterange-syntax.yaml"></a>

```
  [Unit](#cfn-securityhub-automationrule-daterange-unit): String
  [Value](#cfn-securityhub-automationrule-daterange-value): Double
```

## Properties<a name="aws-properties-securityhub-automationrule-daterange-properties"></a>

`Unit`  <a name="cfn-securityhub-automationrule-daterange-unit"></a>
A date range unit for the date filter\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAYS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-securityhub-automationrule-daterange-value"></a>
A date range value for the date filter\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)