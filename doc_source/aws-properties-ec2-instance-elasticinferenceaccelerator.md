# AWS::EC2::Instance ElasticInferenceAccelerator<a name="aws-properties-ec2-instance-elasticinferenceaccelerator"></a>

Specifies the Elastic Inference Accelerator for the instance\.

 `ElasticInferenceAccelerator` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

## Syntax<a name="aws-properties-ec2-instance-elasticinferenceaccelerator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-elasticinferenceaccelerator-syntax.json"></a>

```
{
  "[Type](#cfn-ec2-instance-elasticinferenceaccelerator-type)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-elasticinferenceaccelerator-syntax.yaml"></a>

```
  [Type](#cfn-ec2-instance-elasticinferenceaccelerator-type): String
```

## Properties<a name="aws-properties-ec2-instance-elasticinferenceaccelerator-properties"></a>

`Type`  <a name="cfn-ec2-instance-elasticinferenceaccelerator-type"></a>
 The type of elastic inference accelerator\. The possible values are `eia1.small`, `eia1.medium`, and `eia1.large`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by ***all*** regions.