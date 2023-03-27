# AWS::Config::ConfigRule CustomPolicyDetails<a name="aws-properties-config-configrule-custompolicydetails"></a>

Provides the runtime system, policy definition, and whether debug logging enabled\. You can specify the following CustomPolicyDetails parameter values only for AWS Config Custom Policy rules\.

## Syntax<a name="aws-properties-config-configrule-custompolicydetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configrule-custompolicydetails-syntax.json"></a>

```
{
  "[EnableDebugLogDelivery](#cfn-config-configrule-custompolicydetails-enabledebuglogdelivery)" : Boolean,
  "[PolicyRuntime](#cfn-config-configrule-custompolicydetails-policyruntime)" : String,
  "[PolicyText](#cfn-config-configrule-custompolicydetails-policytext)" : String
}
```

### YAML<a name="aws-properties-config-configrule-custompolicydetails-syntax.yaml"></a>

```
  [EnableDebugLogDelivery](#cfn-config-configrule-custompolicydetails-enabledebuglogdelivery): Boolean
  [PolicyRuntime](#cfn-config-configrule-custompolicydetails-policyruntime): String
  [PolicyText](#cfn-config-configrule-custompolicydetails-policytext): String
```

## Properties<a name="aws-properties-config-configrule-custompolicydetails-properties"></a>

`EnableDebugLogDelivery`  <a name="cfn-config-configrule-custompolicydetails-enabledebuglogdelivery"></a>
The boolean expression for enabling debug logging for your AWS Config Custom Policy rule\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyRuntime`  <a name="cfn-config-configrule-custompolicydetails-policyruntime"></a>
The runtime system for your AWS Config Custom Policy rule\. Guard is a policy\-as\-code language that allows you to write policies that are enforced by AWS Config Custom Policy rules\. For more information about Guard, see the [Guard GitHub Repository](https://github.com/aws-cloudformation/cloudformation-guard)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `guard\-2\.x\.x`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyText`  <a name="cfn-config-configrule-custompolicydetails-policytext"></a>
The policy definition containing the logic for your AWS Config Custom Policy rule\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)