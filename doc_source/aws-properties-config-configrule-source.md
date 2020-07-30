# AWS::Config::ConfigRule Source<a name="aws-properties-config-configrule-source"></a>

Provides the AWS Config rule owner \(AWS or customer\), the rule identifier, and the events that trigger the evaluation of your AWS resources\.

## Syntax<a name="aws-properties-config-configrule-source-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configrule-source-syntax.json"></a>

```
{
  "[Owner](#cfn-config-configrule-source-owner)" : String,
  "[SourceDetails](#cfn-config-configrule-source-sourcedetails)" : [ SourceDetail, ... ],
  "[SourceIdentifier](#cfn-config-configrule-source-sourceidentifier)" : String
}
```

### YAML<a name="aws-properties-config-configrule-source-syntax.yaml"></a>

```
  [Owner](#cfn-config-configrule-source-owner): String
  [SourceDetails](#cfn-config-configrule-source-sourcedetails): 
    - SourceDetail
  [SourceIdentifier](#cfn-config-configrule-source-sourceidentifier): String
```

## Properties<a name="aws-properties-config-configrule-source-properties"></a>

`Owner`  <a name="cfn-config-configrule-source-owner"></a>
Indicates whether AWS or the customer owns and manages the AWS Config rule\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AWS | CUSTOM_LAMBDA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceDetails`  <a name="cfn-config-configrule-source-sourcedetails"></a>
Provides the source and type of the event that causes AWS Config to evaluate your AWS resources\.  
*Required*: No  
*Type*: List of [SourceDetail](aws-properties-config-configrule-source-sourcedetails.md)  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceIdentifier`  <a name="cfn-config-configrule-source-sourceidentifier"></a>
For AWS Config managed rules, a predefined identifier from a list\. For example, `IAM_PASSWORD_POLICY` is a managed rule\. To reference a managed rule, see [Using AWS Managed Config Rules](https://docs.aws.amazon.com/config/latest/developerguide/evaluate-config_use-managed-rules.html)\.  
For custom rules, the identifier is the Amazon Resource Name \(ARN\) of the rule's AWS Lambda function, such as `arn:aws:lambda:us-east-2:123456789012:function:custom_rule_name`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)