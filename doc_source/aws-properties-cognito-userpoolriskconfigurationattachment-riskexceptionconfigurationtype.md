# AWS::Cognito::UserPoolRiskConfigurationAttachment RiskExceptionConfigurationType<a name="aws-properties-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype"></a>

The type of the configuration to override the risk decision\.

## Syntax<a name="aws-properties-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-syntax.json"></a>

```
{
  "[BlockedIPRangeList](#cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-blockediprangelist)" : [ String, ... ],
  "[SkippedIPRangeList](#cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-skippediprangelist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-syntax.yaml"></a>

```
  [BlockedIPRangeList](#cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-blockediprangelist): 
    - String
  [SkippedIPRangeList](#cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-skippediprangelist): 
    - String
```

## Properties<a name="aws-properties-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-properties"></a>

`BlockedIPRangeList`  <a name="cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-blockediprangelist"></a>
Overrides the risk decision to always block the pre\-authentication requests\. The IP range is in CIDR notation: a compact representation of an IP address and its associated routing prefix\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SkippedIPRangeList`  <a name="cfn-cognito-userpoolriskconfigurationattachment-riskexceptionconfigurationtype-skippediprangelist"></a>
Risk detection is not performed on the IP addresses in the range list\. The IP range is in CIDR notation\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)