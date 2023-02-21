# AWS::Config::ConfigRule Source<a name="aws-properties-config-configrule-source"></a>

Provides the CustomPolicyDetails, the rule owner \(` AWS ` for managed rules, `CUSTOM_POLICY` for Custom Policy rules, and `CUSTOM_LAMBDA` for Custom Lambda rules\), the rule identifier, and the events that cause the evaluation of your AWS resources\.

## Syntax<a name="aws-properties-config-configrule-source-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configrule-source-syntax.json"></a>

```
{
  "[CustomPolicyDetails](#cfn-config-configrule-source-custompolicydetails)" : CustomPolicyDetails,
  "[Owner](#cfn-config-configrule-source-owner)" : String,
  "[SourceDetails](#cfn-config-configrule-source-sourcedetails)" : [ SourceDetail, ... ],
  "[SourceIdentifier](#cfn-config-configrule-source-sourceidentifier)" : String
}
```

### YAML<a name="aws-properties-config-configrule-source-syntax.yaml"></a>

```
  [CustomPolicyDetails](#cfn-config-configrule-source-custompolicydetails): 
    CustomPolicyDetails
  [Owner](#cfn-config-configrule-source-owner): String
  [SourceDetails](#cfn-config-configrule-source-sourcedetails): 
    - SourceDetail
  [SourceIdentifier](#cfn-config-configrule-source-sourceidentifier): String
```

## Properties<a name="aws-properties-config-configrule-source-properties"></a>

`CustomPolicyDetails`  <a name="cfn-config-configrule-source-custompolicydetails"></a>
Provides the runtime system, policy definition, and whether debug logging is enabled\. Required when owner is set to `CUSTOM_POLICY`\.  
*Required*: No  
*Type*: [CustomPolicyDetails](aws-properties-config-configrule-custompolicydetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Owner`  <a name="cfn-config-configrule-source-owner"></a>
Indicates whether AWS or the customer owns and manages the AWS Config rule\.  
 AWS Config Managed Rules are predefined rules owned by AWS\. For more information, see [AWS Config Managed Rules](https://docs.aws.amazon.com/config/latest/developerguide/evaluate-config_use-managed-rules.html) in the * AWS Config developer guide*\.  
 AWS Config Custom Rules are rules that you can develop either with Guard \(`CUSTOM_POLICY`\) or AWS Lambda \(`CUSTOM_LAMBDA`\)\. For more information, see [AWS Config Custom Rules ](https://docs.aws.amazon.com/config/latest/developerguide/evaluate-config_develop-rules.html) in the * AWS Config developer guide*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AWS | CUSTOM_LAMBDA | CUSTOM_POLICY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceDetails`  <a name="cfn-config-configrule-source-sourcedetails"></a>
Provides the source and the message types that cause AWS Config to evaluate your AWS resources against a rule\. It also provides the frequency with which you want AWS Config to run evaluations for the rule if the trigger type is periodic\.  
If the owner is set to `CUSTOM_POLICY`, the only acceptable values for the AWS Config rule trigger message type are `ConfigurationItemChangeNotification` and `OversizedConfigurationItemChangeNotification`\.  
*Required*: No  
*Type*: List of [SourceDetail](aws-properties-config-configrule-source-sourcedetails.md)  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceIdentifier`  <a name="cfn-config-configrule-source-sourceidentifier"></a>
For AWS Config Managed rules, a predefined identifier from a list\. For example, `IAM_PASSWORD_POLICY` is a managed rule\. To reference a managed rule, see [List of AWS Config Managed Rules](https://docs.aws.amazon.com/config/latest/developerguide/managed-rules-by-aws-config.html)\.  
For AWS Config Custom Lambda rules, the identifier is the Amazon Resource Name \(ARN\) of the rule's AWS Lambda function, such as `arn:aws:lambda:us-east-2:123456789012:function:custom_rule_name`\.  
For AWS Config Custom Policy rules, this field will be ignored\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)