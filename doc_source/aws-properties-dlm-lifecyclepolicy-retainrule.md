# AWS::DLM::LifecyclePolicy RetainRule<a name="aws-properties-dlm-lifecyclepolicy-retainrule"></a>

Specifies the number of snapshots to keep for each EBS volume\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-retainrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-retainrule-syntax.json"></a>

```
{
  "[Count](#cfn-dlm-lifecyclepolicy-retainrule-count)" : Integer
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-retainrule-syntax.yaml"></a>

```
  [Count](#cfn-dlm-lifecyclepolicy-retainrule-count): Integer
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-retainrule-properties"></a>

`Count`  <a name="cfn-dlm-lifecyclepolicy-retainrule-count"></a>
The number of snapshots to keep for each volume, up to a maximum of 1000\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)