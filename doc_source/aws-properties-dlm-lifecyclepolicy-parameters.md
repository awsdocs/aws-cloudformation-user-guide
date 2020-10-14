# AWS::DLM::LifecyclePolicy Parameters<a name="aws-properties-dlm-lifecyclepolicy-parameters"></a>

Specifies optional parameters to add to a policy\. The set of valid parameters depends on the combination of policy type and resource type\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-parameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-parameters-syntax.json"></a>

```
{
  "[ExcludeBootVolume](#cfn-dlm-lifecyclepolicy-parameters-excludebootvolume)" : Boolean
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-parameters-syntax.yaml"></a>

```
  [ExcludeBootVolume](#cfn-dlm-lifecyclepolicy-parameters-excludebootvolume): Boolean
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-parameters-properties"></a>

`ExcludeBootVolume`  <a name="cfn-dlm-lifecyclepolicy-parameters-excludebootvolume"></a>
\[EBS Snapshot Management – Instance policies only\] Indicates whether to exclude the root volume from snapshots created using [CreateSnapshots](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateSnapshots.html)\. The default is false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)