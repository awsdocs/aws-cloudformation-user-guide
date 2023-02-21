# AWS::Pipes::Pipe EcsInferenceAcceleratorOverride<a name="aws-properties-pipes-pipe-ecsinferenceacceleratoroverride"></a>

Details on an Elastic Inference accelerator task override\. This parameter is used to override the Elastic Inference accelerator specified in the task definition\. For more information, see [Working with Amazon Elastic Inference on Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/userguide/ecs-inference.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-pipes-pipe-ecsinferenceacceleratoroverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-ecsinferenceacceleratoroverride-syntax.json"></a>

```
{
  "[DeviceName](#cfn-pipes-pipe-ecsinferenceacceleratoroverride-devicename)" : String,
  "[DeviceType](#cfn-pipes-pipe-ecsinferenceacceleratoroverride-devicetype)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-ecsinferenceacceleratoroverride-syntax.yaml"></a>

```
  [DeviceName](#cfn-pipes-pipe-ecsinferenceacceleratoroverride-devicename): String
  [DeviceType](#cfn-pipes-pipe-ecsinferenceacceleratoroverride-devicetype): String
```

## Properties<a name="aws-properties-pipes-pipe-ecsinferenceacceleratoroverride-properties"></a>

`DeviceName`  <a name="cfn-pipes-pipe-ecsinferenceacceleratoroverride-devicename"></a>
The Elastic Inference accelerator device name to override for the task\. This parameter must match a `deviceName` specified in the task definition\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceType`  <a name="cfn-pipes-pipe-ecsinferenceacceleratoroverride-devicetype"></a>
The Elastic Inference accelerator type to use\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)