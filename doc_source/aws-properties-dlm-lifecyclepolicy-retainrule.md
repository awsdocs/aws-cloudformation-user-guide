# Amazon Data Lifecycle Manager LifecyclePolicy RetainRule<a name="aws-properties-dlm-lifecyclepolicy-retainrule"></a>

<a name="aws-properties-dlm-lifecyclepolicy-retainrule-description"></a>The `RetainRule` property type specifies a snapshot retention rule for an Amazon Data Lifecycle Manager lifecycle policy\.

<a name="aws-properties-dlm-lifecyclepolicy-retainrule-inheritance"></a> `RetainRule` is a property of the [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md) property type\.

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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-dlm-lifecyclepolicy-retainrule-seealso"></a>
+ [Automating the Amazon EBS Snapshot Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html) in the Amazon EC2 User Guide for Linux Instances
+ [RetainRule](https://docs.aws.amazon.com/dlm/latest/APIReference/API_RetainRule.html) in the Amazon Data Lifecycle Manager API Reference