# Amazon Data Lifecycle Manager LifecyclePolicy CreateRule<a name="aws-properties-dlm-lifecyclepolicy-createrule"></a>

<a name="aws-properties-dlm-lifecyclepolicy-createrule-description"></a>The `CreateRule` property type specifies when to create snapshots of EBS volumes\.

<a name="aws-properties-dlm-lifecyclepolicy-createrule-inheritance"></a> `CreateRule` is a property of the [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md) property type\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.json"></a>

```
{
  "[Interval](#cfn-dlm-lifecyclepolicy-createrule-interval)" : Integer,
  "[IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit)" : String,
  "[Times](#cfn-dlm-lifecyclepolicy-createrule-times)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-createrule-syntax.yaml"></a>

```
[Interval](#cfn-dlm-lifecyclepolicy-createrule-interval): Integer
[IntervalUnit](#cfn-dlm-lifecyclepolicy-createrule-intervalunit): String
[Times](#cfn-dlm-lifecyclepolicy-createrule-times): 
  - String
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-createrule-properties"></a>

`Interval`  <a name="cfn-dlm-lifecyclepolicy-createrule-interval"></a>
The time interval between snapshots\. Supported values are `12` and `24`\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`IntervalUnit`  <a name="cfn-dlm-lifecyclepolicy-createrule-intervalunit"></a>
The time unit\. The supported unit is `HOURS`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Times`  <a name="cfn-dlm-lifecyclepolicy-createrule-times"></a>
The time, in UTC, to start the operation\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-dlm-lifecyclepolicy-createrule-seealso"></a>
+ [Automating the Amazon EBS Snapshot Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html) in the Amazon EC2 User Guide for Linux Instances
+ [CreateRule](https://docs.aws.amazon.com/dlm/latest/APIReference/API_CreateRule.html) in the Amazon Data Lifecycle Manager API Reference