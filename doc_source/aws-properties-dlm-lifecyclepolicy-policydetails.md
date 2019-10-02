# AWS::DLM::LifecyclePolicy PolicyDetails<a name="aws-properties-dlm-lifecyclepolicy-policydetails"></a>

Specifies the configuration of a lifecycle policy\.

## Syntax<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.json"></a>

```
{
  "[ResourceTypes](#cfn-dlm-lifecyclepolicy-policydetails-resourcetypes)" : [ String, ... ],
  "[Schedules](#cfn-dlm-lifecyclepolicy-policydetails-schedules)" : [ [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md), ... ],
  "[TargetTags](#cfn-dlm-lifecyclepolicy-policydetails-targettags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-dlm-lifecyclepolicy-policydetails-syntax.yaml"></a>

```
  [ResourceTypes](#cfn-dlm-lifecyclepolicy-policydetails-resourcetypes): 
    - String
  [Schedules](#cfn-dlm-lifecyclepolicy-policydetails-schedules): 
    - [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md)
  [TargetTags](#cfn-dlm-lifecyclepolicy-policydetails-targettags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-dlm-lifecyclepolicy-policydetails-properties"></a>

`ResourceTypes`  <a name="cfn-dlm-lifecyclepolicy-policydetails-resourcetypes"></a>
The resource type\. Specify one of `INSTANCE` or `VOLUME`\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedules`  <a name="cfn-dlm-lifecyclepolicy-policydetails-schedules"></a>
The schedule of policy\-defined actions\.  
*Required*: No  
*Type*: List of [Schedule](aws-properties-dlm-lifecyclepolicy-schedule.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTags`  <a name="cfn-dlm-lifecyclepolicy-policydetails-targettags"></a>
The single tag that identifies targeted resources for this policy\.  
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
