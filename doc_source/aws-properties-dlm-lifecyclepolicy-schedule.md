# Amazon Data Lifecycle Manager LifecyclePolicy Schedule<a name="aws-properties-dlm-lifecyclepolicy-schedule"></a>

<a name="aws-properties-dlm-lifecyclepolicy-schedule-description"></a>The `Schedule` property type specifies a backup schedule for an Amazon Data Lifecycle Manager lifecycle policy\.

<a name="aws-properties-dlm-lifecyclepolicy-schedule-inheritance"></a> `Schedule` is a property of the [PolicyDetails](aws-properties-dlm-lifecyclepolicy-policydetails.md) property type\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax.json"></a>

```
{
  "[CopyTags](#cfn-dlm-lifecyclepolicy-schedule-copytags)" : Boolean,
  "[CreateRule](#cfn-dlm-lifecyclepolicy-schedule-createrule)" : [*CreateRule*](aws-properties-dlm-lifecyclepolicy-createrule.md),
  "[Name](#cfn-dlm-lifecyclepolicy-schedule-name)" : String,
  "[RetainRule](#cfn-dlm-lifecyclepolicy-schedule-retainrule)" : [*RetainRule*](aws-properties-dlm-lifecyclepolicy-retainrule.md),
  "[TagsToAdd](#cfn-dlm-lifecyclepolicy-schedule-tagstoadd)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax.yaml"></a>

```
[CopyTags](#cfn-dlm-lifecyclepolicy-schedule-copytags): Boolean
[CreateRule](#cfn-dlm-lifecyclepolicy-schedule-createrule): 
  [*CreateRule*](aws-properties-dlm-lifecyclepolicy-createrule.md)
[Name](#cfn-dlm-lifecyclepolicy-schedule-name): String
[RetainRule](#cfn-dlm-lifecyclepolicy-schedule-retainrule): 
  [*RetainRule*](aws-properties-dlm-lifecyclepolicy-retainrule.md)
[TagsToAdd](#cfn-dlm-lifecyclepolicy-schedule-tagstoadd): 
  - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-schedule-properties"></a>

`CopyTags`  <a name="cfn-dlm-lifecyclepolicy-schedule-copytags"></a>
Copy all user\-defined tags on a source volume to snapshots of the volume created by a policy\.   
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CreateRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-createrule"></a>
The create rule for a policy\.  
 *Required*: No  
 *Type*: [CreateRule](aws-properties-dlm-lifecyclepolicy-createrule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-dlm-lifecyclepolicy-schedule-name"></a>
The name of the schedule\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RetainRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-retainrule"></a>
The retention rule for a policy\.  
 *Required*: No  
 *Type*: [RetainRule](aws-properties-dlm-lifecyclepolicy-retainrule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TagsToAdd`  <a name="cfn-dlm-lifecyclepolicy-schedule-tagstoadd"></a>
The tags to apply to policy\-created resources\. These user\-defined tags are in addition to the AWS\-added lifecycle tags\.   
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-dlm-lifecyclepolicy-schedule-seealso"></a>
+ [Automating the Amazon EBS Snapshot Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html) in the Amazon EC2 User Guide for Linux Instances
+ [Schedule](https://docs.aws.amazon.com/dlm/latest/APIReference/API_Schedule.html) in the Amazon Data Lifecycle Manager API Reference