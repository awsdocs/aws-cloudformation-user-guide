# AWS::ECS::TaskDefinition InferenceAccelerator<a name="aws-properties-ecs-taskdefinition-inferenceaccelerator"></a>

Details on an Elastic Inference accelerator\. For more information, see [Working with Amazon Elastic Inference on Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-eia.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-taskdefinition-inferenceaccelerator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-inferenceaccelerator-syntax.json"></a>

```
{
  "[DeviceName](#cfn-ecs-taskdefinition-inferenceaccelerator-devicename)" : String,
  "[DeviceType](#cfn-ecs-taskdefinition-inferenceaccelerator-devicetype)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-inferenceaccelerator-syntax.yaml"></a>

```
  [DeviceName](#cfn-ecs-taskdefinition-inferenceaccelerator-devicename): String
  [DeviceType](#cfn-ecs-taskdefinition-inferenceaccelerator-devicetype): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-inferenceaccelerator-properties"></a>

`DeviceName`  <a name="cfn-ecs-taskdefinition-inferenceaccelerator-devicename"></a>
The Elastic Inference accelerator device name\. The `deviceName` must also be referenced in a container definition as a [ResourceRequirement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-resourcerequirement.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeviceType`  <a name="cfn-ecs-taskdefinition-inferenceaccelerator-devicetype"></a>
The Elastic Inference accelerator type to use\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)