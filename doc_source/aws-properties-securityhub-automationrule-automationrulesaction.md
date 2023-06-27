# AWS::SecurityHub::AutomationRule AutomationRulesAction<a name="aws-properties-securityhub-automationrule-automationrulesaction"></a>

 One or more actions to update finding fields if a finding matches the defined criteria of the rule\. 

## Syntax<a name="aws-properties-securityhub-automationrule-automationrulesaction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-automationrulesaction-syntax.json"></a>

```
{
  "[FindingFieldsUpdate](#cfn-securityhub-automationrule-automationrulesaction-findingfieldsupdate)" : AutomationRulesFindingFieldsUpdate,
  "[Type](#cfn-securityhub-automationrule-automationrulesaction-type)" : String
}
```

### YAML<a name="aws-properties-securityhub-automationrule-automationrulesaction-syntax.yaml"></a>

```
  [FindingFieldsUpdate](#cfn-securityhub-automationrule-automationrulesaction-findingfieldsupdate): 
    AutomationRulesFindingFieldsUpdate
  [Type](#cfn-securityhub-automationrule-automationrulesaction-type): String
```

## Properties<a name="aws-properties-securityhub-automationrule-automationrulesaction-properties"></a>

`FindingFieldsUpdate`  <a name="cfn-securityhub-automationrule-automationrulesaction-findingfieldsupdate"></a>
 Specifies that the automation rule action is an update to a finding field\.   
*Required*: Yes  
*Type*: [AutomationRulesFindingFieldsUpdate](aws-properties-securityhub-automationrule-automationrulesfindingfieldsupdate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-securityhub-automationrule-automationrulesaction-type"></a>
 Specifies that the rule action should update the `Types` finding field\. The `Types` finding field classifies findings in the format of namespace/category/classifier\. For more information, see [Types taxonomy for ASFF](https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-findings-format-type-taxonomy.html) in the * AWS Security Hub User Guide*\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `FINDING_FIELDS_UPDATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)