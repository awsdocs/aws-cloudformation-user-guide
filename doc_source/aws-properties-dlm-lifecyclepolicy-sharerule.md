# AWS::DLM::LifecyclePolicy ShareRule<a name="aws-properties-dlm-lifecyclepolicy-sharerule"></a>

Specifies a rule for sharing snapshots across AWS accounts\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-sharerule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-sharerule-syntax.json"></a>

```
{
  "[TargetAccounts](#cfn-dlm-lifecyclepolicy-sharerule-targetaccounts)" : [ String, ... ],
  "[UnshareInterval](#cfn-dlm-lifecyclepolicy-sharerule-unshareinterval)" : Integer,
  "[UnshareIntervalUnit](#cfn-dlm-lifecyclepolicy-sharerule-unshareintervalunit)" : String
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-sharerule-syntax.yaml"></a>

```
  [TargetAccounts](#cfn-dlm-lifecyclepolicy-sharerule-targetaccounts): 
    - String
  [UnshareInterval](#cfn-dlm-lifecyclepolicy-sharerule-unshareinterval): Integer
  [UnshareIntervalUnit](#cfn-dlm-lifecyclepolicy-sharerule-unshareintervalunit): String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-sharerule-properties"></a>

`TargetAccounts`  <a name="cfn-dlm-lifecyclepolicy-sharerule-targetaccounts"></a>
The IDs of the AWS accounts with which to share the snapshots\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnshareInterval`  <a name="cfn-dlm-lifecyclepolicy-sharerule-unshareinterval"></a>
The period after which snapshots that are shared with other AWS accounts are automatically unshared\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnshareIntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-sharerule-unshareintervalunit"></a>
The unit of time for the automatic unsharing interval\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAYS | MONTHS | WEEKS | YEARS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)