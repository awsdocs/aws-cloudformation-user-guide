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
