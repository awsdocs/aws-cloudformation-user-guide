# Amazon Data Lifecycle Manager LifecyclePolicy PolicyDetails<a name="aws-properties-dlm-lifecyclepolicy-policydetails"></a>

<a name="aws-properties-dlm-lifecyclepolicy-policydetails-description"></a>The `PolicyDetails` property type specifies details for an Amazon Data Lifecycle Manager lifecycle policy\.

<a name="aws-properties-dlm-lifecyclepolicy-policydetails-inheritance"></a> `PolicyDetails` is a property of the [AWS::DLM::LifecyclePolicy](aws-resource-dlm-lifecyclepolicy.md) resource type\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.json"></a>

```
{
  "[ResourceTypes](#cfn-dlm-lifecyclepolicy-policydetails-resourcetypes)" : [ String, ... ],
  "[Schedules](#cfn-dlm-lifecyclepolicy-policydetails-schedules)" : [ [*Schedule*](aws-properties-dlm-lifecyclepolicy-schedule.md), ... ],
  "[TargetTags](#cfn-dlm-lifecyclepolicy-policydetails-targettags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.yaml"></a>

```
[ResourceTypes](#cfn-dlm-lifecyclepolicy-policydetails-resourcetypes): 
  - String
[Schedules](#cfn-dlm-lifecyclepolicy-policydetails-schedules): 
  - [*Schedule*](aws-properties-dlm-lifecyclepolicy-schedule.md)
[TargetTags](#cfn-dlm-lifecyclepolicy-policydetails-targettags): 
  - [*Tag*](aws-properties-resource-tags.md)
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-policydetails-properties"></a>

`ResourceTypes`  <a name="cfn-dlm-lifecyclepolicy-policydetails-resourcetypes"></a>
The type of AWS resource\. The supported value is `VOLUME`\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Schedules`  <a name="cfn-dlm-lifecyclepolicy-policydetails-schedules"></a>
The schedule of policy\-defined actions\.  
 *Required*: No  
 *Type*: List of [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetTags`  <a name="cfn-dlm-lifecyclepolicy-policydetails-targettags"></a>
The single tag that identifies targeted resources for a policy\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-dlm-lifecyclepolicy-policydetails-seealso"></a>
+ [Automating the Amazon EBS Snapshot Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html) in the Amazon EC2 User Guide for Linux Instances
+ [PolicyDetails](https://docs.aws.amazon.com/dlm/latest/APIReference/API_PolicyDetails.html) in the Amazon Data Lifecycle Manager API Reference