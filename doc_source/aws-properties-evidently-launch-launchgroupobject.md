# AWS::Evidently::Launch LaunchGroupObject<a name="aws-properties-evidently-launch-launchgroupobject"></a>

A structure that defines one launch group in a launch\. A launch group is a variation of the feature that you are including in the launch\.

## Syntax<a name="aws-properties-evidently-launch-launchgroupobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-launch-launchgroupobject-syntax.json"></a>

```
{
  "[Description](#cfn-evidently-launch-launchgroupobject-description)" : String,
  "[Feature](#cfn-evidently-launch-launchgroupobject-feature)" : String,
  "[GroupName](#cfn-evidently-launch-launchgroupobject-groupname)" : String,
  "[Variation](#cfn-evidently-launch-launchgroupobject-variation)" : String
}
```

### YAML<a name="aws-properties-evidently-launch-launchgroupobject-syntax.yaml"></a>

```
  [Description](#cfn-evidently-launch-launchgroupobject-description): String
  [Feature](#cfn-evidently-launch-launchgroupobject-feature): String
  [GroupName](#cfn-evidently-launch-launchgroupobject-groupname): String
  [Variation](#cfn-evidently-launch-launchgroupobject-variation): String
```

## Properties<a name="aws-properties-evidently-launch-launchgroupobject-properties"></a>

`Description`  <a name="cfn-evidently-launch-launchgroupobject-description"></a>
A description of the launch group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Feature`  <a name="cfn-evidently-launch-launchgroupobject-feature"></a>
The feature that this launch is using\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupName`  <a name="cfn-evidently-launch-launchgroupobject-groupname"></a>
A name for this launch group\. It can include up to 127 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variation`  <a name="cfn-evidently-launch-launchgroupobject-variation"></a>
The feature variation to use for this launch group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)