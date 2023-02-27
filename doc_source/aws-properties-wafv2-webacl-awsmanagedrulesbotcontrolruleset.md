# AWS::WAFv2::WebACL AWSManagedRulesBotControlRuleSet<a name="aws-properties-wafv2-webacl-awsmanagedrulesbotcontrolruleset"></a>

Details for your use of the Bot Control managed rule group, used in `ManagedRuleGroupConfig`\. 

## Syntax<a name="aws-properties-wafv2-webacl-awsmanagedrulesbotcontrolruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-awsmanagedrulesbotcontrolruleset-syntax.json"></a>

```
{
  "[InspectionLevel](#cfn-wafv2-webacl-awsmanagedrulesbotcontrolruleset-inspectionlevel)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-awsmanagedrulesbotcontrolruleset-syntax.yaml"></a>

```
  [InspectionLevel](#cfn-wafv2-webacl-awsmanagedrulesbotcontrolruleset-inspectionlevel): String
```

## Properties<a name="aws-properties-wafv2-webacl-awsmanagedrulesbotcontrolruleset-properties"></a>

`InspectionLevel`  <a name="cfn-wafv2-webacl-awsmanagedrulesbotcontrolruleset-inspectionlevel"></a>
The inspection level to use for the Bot Control rule group\. The common level is the least expensive\. The targeted level includes all common level rules and adds rules with more advanced inspection criteria\. For details, see [AWS WAF Bot Control rule group](https://docs.aws.amazon.com/waf/latest/developerguide/aws-managed-rule-groups-bot.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)