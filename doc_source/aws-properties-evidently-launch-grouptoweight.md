# AWS::Evidently::Launch GroupToWeight<a name="aws-properties-evidently-launch-grouptoweight"></a>

A structure containing the percentage of launch traffic to allocate to one launch group\.

## Syntax<a name="aws-properties-evidently-launch-grouptoweight-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-launch-grouptoweight-syntax.json"></a>

```
{
  "[GroupName](#cfn-evidently-launch-grouptoweight-groupname)" : String,
  "[SplitWeight](#cfn-evidently-launch-grouptoweight-splitweight)" : Integer
}
```

### YAML<a name="aws-properties-evidently-launch-grouptoweight-syntax.yaml"></a>

```
  [GroupName](#cfn-evidently-launch-grouptoweight-groupname): String
  [SplitWeight](#cfn-evidently-launch-grouptoweight-splitweight): Integer
```

## Properties<a name="aws-properties-evidently-launch-grouptoweight-properties"></a>

`GroupName`  <a name="cfn-evidently-launch-grouptoweight-groupname"></a>
The name of the launch group\. It can include up to 127 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SplitWeight`  <a name="cfn-evidently-launch-grouptoweight-splitweight"></a>
The portion of launch traffic to allocate to this launch group\.  
This is represented in thousandths of a percent\. For example, specify 20,000 to allocate 20% of the launch audience to this launch group\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)