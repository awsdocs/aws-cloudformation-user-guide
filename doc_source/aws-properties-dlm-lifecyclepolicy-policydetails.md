# AWS::DLM::LifecyclePolicy PolicyDetails<a name="aws-properties-dlm-lifecyclepolicy-policydetails"></a>

Specifies the configuration of a lifecycle policy\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.json"></a>

```
{
  "[Parameters](#cfn-dlm-lifecyclepolicy-policydetails-parameters)" : Parameters,
  "[PolicyType](#cfn-dlm-lifecyclepolicy-policydetails-policytype)" : String,
  "[ResourceTypes](#cfn-dlm-lifecyclepolicy-policydetails-resourcetypes)" : [ String, ... ],
  "[Schedules](#cfn-dlm-lifecyclepolicy-policydetails-schedules)" : [ Schedule, ... ],
  "[TargetTags](#cfn-dlm-lifecyclepolicy-policydetails-targettags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.yaml"></a>

```
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

`Parameters`  <a name="cfn-dlm-lifecyclepolicy-policydetails-parameters"></a>
A set of optional parameters for the policy\.   
*Required*: No  
*Type*: [Parameters](aws-properties-dlm-lifecyclepolicy-parameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyType`  <a name="cfn-dlm-lifecyclepolicy-policydetails-policytype"></a>
The valid target resource types and actions a policy can manage\. The default is EBS\_SNAPSHOT\_MANAGEMENT\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EBS_SNAPSHOT_MANAGEMENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTypes`  <a name="cfn-dlm-lifecyclepolicy-policydetails-resourcetypes"></a>
The resource type\. Use VOLUME to create snapshots of individual volumes or use INSTANCE to create multi\-volume snapshots from the volumes for an instance\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedules`  <a name="cfn-dlm-lifecyclepolicy-policydetails-schedules"></a>
The schedule of policy\-defined actions\.  
*Required*: Yes  
*Type*: List of [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTags`  <a name="cfn-dlm-lifecyclepolicy-policydetails-targettags"></a>
The single tag that identifies targeted resources for this policy\.  
*Required*: Yes  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-dlm-lifecyclepolicy-policydetails--seealso"></a>
+  [PolicyDetails](https://docs.aws.amazon.com/dlm/latest/APIReference/API_PolicyDetails.html) in the *Amazon Data Lifecycle Manager API Reference* 