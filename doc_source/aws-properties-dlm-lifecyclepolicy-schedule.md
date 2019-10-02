# AWS::DLM::LifecyclePolicy Schedule<a name="aws-properties-dlm-lifecyclepolicy-schedule"></a>

Specifies a backup schedule\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax.json"></a>

```
{
  "[CopyTags](#cfn-dlm-lifecyclepolicy-schedule-copytags)" : Boolean,
  "[CreateRule](#cfn-dlm-lifecyclepolicy-schedule-createrule)" : [CreateRule](aws-properties-dlm-lifecyclepolicy-createrule.md),
  "[Name](#cfn-dlm-lifecyclepolicy-schedule-name)" : String,
  "[RetainRule](#cfn-dlm-lifecyclepolicy-schedule-retainrule)" : [RetainRule](aws-properties-dlm-lifecyclepolicy-retainrule.md),
  "[TagsToAdd](#cfn-dlm-lifecyclepolicy-schedule-tagstoadd)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-schedule-syntax.yaml"></a>

```
  [CopyTags](#cfn-dlm-lifecyclepolicy-schedule-copytags): Boolean
  [CreateRule](#cfn-dlm-lifecyclepolicy-schedule-createrule): 
    [CreateRule](aws-properties-dlm-lifecyclepolicy-createrule.md)
  [Name](#cfn-dlm-lifecyclepolicy-schedule-name): String
  [RetainRule](#cfn-dlm-lifecyclepolicy-schedule-retainrule): 
    [RetainRule](aws-properties-dlm-lifecyclepolicy-retainrule.md)
  [TagsToAdd](#cfn-dlm-lifecyclepolicy-schedule-tagstoadd): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-schedule-properties"></a>

`CopyTags`  <a name="cfn-dlm-lifecyclepolicy-schedule-copytags"></a>
Copy all user\-defined tags on a source volume to snapshots of the volume created by this policy\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-createrule"></a>
The create rule\.  
*Required*: No  
*Type*: [CreateRule](aws-properties-dlm-lifecyclepolicy-createrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-dlm-lifecyclepolicy-schedule-name"></a>
The name of the schedule\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetainRule`  <a name="cfn-dlm-lifecyclepolicy-schedule-retainrule"></a>
The retain rule\.  
*Required*: No  
*Type*: [RetainRule](aws-properties-dlm-lifecyclepolicy-retainrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagsToAdd`  <a name="cfn-dlm-lifecyclepolicy-schedule-tagstoadd"></a>
The tags to apply to policy\-created resources\. These user\-defined tags are in addition to the AWS\-added lifecycle tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
