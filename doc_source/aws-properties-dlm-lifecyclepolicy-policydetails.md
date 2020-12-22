# AWS::DLM::LifecyclePolicy PolicyDetails<a name="aws-properties-dlm-lifecyclepolicy-policydetails"></a>

Specifies the configuration of a lifecycle policy\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.json"></a>

```
{
  "[Actions](#cfn-dlm-lifecyclepolicy-policydetails-actions)" : [ Action, ... ],
  "[EventSource](#cfn-dlm-lifecyclepolicy-policydetails-eventsource)" : EventSource,
  "[Parameters](#cfn-dlm-lifecyclepolicy-policydetails-parameters)" : Parameters,
  "[PolicyType](#cfn-dlm-lifecyclepolicy-policydetails-policytype)" : String,
  "[ResourceTypes](#cfn-dlm-lifecyclepolicy-policydetails-resourcetypes)" : [ String, ... ],
  "[Schedules](#cfn-dlm-lifecyclepolicy-policydetails-schedules)" : [ Schedule, ... ],
  "[TargetTags](#cfn-dlm-lifecyclepolicy-policydetails-targettags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.yaml"></a>

```
  [Actions](#cfn-dlm-lifecyclepolicy-policydetails-actions): 
    - Action
  [EventSource](#cfn-dlm-lifecyclepolicy-policydetails-eventsource): 
    EventSource
  [Parameters](#cfn-dlm-lifecyclepolicy-policydetails-parameters): 
    Parameters
  [PolicyType](#cfn-dlm-lifecyclepolicy-policydetails-policytype): String
  [ResourceTypes](#cfn-dlm-lifecyclepolicy-policydetails-resourcetypes): 
    - String
  [Schedules](#cfn-dlm-lifecyclepolicy-policydetails-schedules): 
    - Schedule
  [TargetTags](#cfn-dlm-lifecyclepolicy-policydetails-targettags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-policydetails-properties"></a>

`Actions`  <a name="cfn-dlm-lifecyclepolicy-policydetails-actions"></a>
The actions to be performed when the event\-based policy is triggered\. You can specify only one action per policy\.  
This parameter is required for event\-based policies only\. If you are creating a snapshot or AMI policy, omit this parameter\.  
*Required*: No  
*Type*: List of [Action](aws-properties-dlm-lifecyclepolicy-action.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventSource`  <a name="cfn-dlm-lifecyclepolicy-policydetails-eventsource"></a>
The event that triggers the event\-based policy\.   
This parameter is required for event\-based policies only\. If you are creating a snapshot or AMI policy, omit this parameter\.  
*Required*: No  
*Type*: [EventSource](aws-properties-dlm-lifecyclepolicy-eventsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-dlm-lifecyclepolicy-policydetails-parameters"></a>
A set of optional parameters for snapshot and AMI lifecycle policies\.   
This parameter is required for snapshot and AMI policies only\. If you are creating an event\-based policy, omit this parameter\.  
*Required*: No  
*Type*: [Parameters](aws-properties-dlm-lifecyclepolicy-parameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyType`  <a name="cfn-dlm-lifecyclepolicy-policydetails-policytype"></a>
The valid target resource types and actions a policy can manage\. Specify `EBS_SNAPSHOT_MANAGEMENT` to create a lifecycle policy that manages the lifecycle of Amazon EBS snapshots\. Specify `IMAGE_MANAGEMENT` to create a lifecycle policy that manages the lifecycle of EBS\-backed AMIs\. Specify `EVENT_BASED_POLICY ` to create an event\-based policy that performs specific actions when a defined event occurs in your AWS account\.  
The default is `EBS_SNAPSHOT_MANAGEMENT`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EBS_SNAPSHOT_MANAGEMENT | EVENT_BASED_POLICY | IMAGE_MANAGEMENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTypes`  <a name="cfn-dlm-lifecyclepolicy-policydetails-resourcetypes"></a>
The target resource type for snapshot and AMI lifecycle policies\. Use `VOLUME `to create snapshots of individual volumes or use `INSTANCE` to create multi\-volume snapshots from the volumes for an instance\.  
This parameter is required for snapshot and AMI policies only\. If you are creating an event\-based policy, omit this parameter\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedules`  <a name="cfn-dlm-lifecyclepolicy-policydetails-schedules"></a>
The schedules of policy\-defined actions for snapshot and AMI lifecycle policies\. A policy can have up to four schedules—one mandatory schedule and up to three optional schedules\.  
This parameter is required for snapshot and AMI policies only\. If you are creating an event\-based policy, omit this parameter\.  
*Required*: No  
*Type*: List of [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md)  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTags`  <a name="cfn-dlm-lifecyclepolicy-policydetails-targettags"></a>
The single tag that identifies targeted resources for this policy\.  
This parameter is required for snapshot and AMI policies only\. If you are creating an event\-based policy, omit this parameter\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-dlm-lifecyclepolicy-policydetails--seealso"></a>
+  [PolicyDetails](https://docs.aws.amazon.com/dlm/latest/APIReference/API_PolicyDetails.html) in the *Amazon Data Lifecycle Manager API Reference* 

