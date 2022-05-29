# AWS::ECS::TaskDefinition EphemeralStorage<a name="aws-properties-ecs-taskdefinition-ephemeralstorage"></a>

The amount of ephemeral storage to allocate for the task\. This parameter is used to expand the total amount of ephemeral storage available, beyond the default amount, for tasks hosted on AWS Fargate\. For more information, see [Fargate task storage](https://docs.aws.amazon.com/AmazonECS/latest/userguide/using_data_volumes.html) in the *Amazon ECS User Guide for AWS Fargate *\.

**Note**  
This parameter is only supported for tasks hosted on Fargate using Linux platform version `1.4.0` or later\. This parameter is not supported for Windows containers on Fargate\.

## Syntax<a name="aws-properties-ecs-taskdefinition-ephemeralstorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-ephemeralstorage-syntax.json"></a>

```
{
  "[SizeInGiB](#cfn-ecs-taskdefinition-ephemeralstorage-sizeingib)" : Integer
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-ephemeralstorage-syntax.yaml"></a>

```
  [SizeInGiB](#cfn-ecs-taskdefinition-ephemeralstorage-sizeingib): Integer
```

## Properties<a name="aws-properties-ecs-taskdefinition-ephemeralstorage-properties"></a>

`SizeInGiB`  <a name="cfn-ecs-taskdefinition-ephemeralstorage-sizeingib"></a>
The total amount, in GiB, of ephemeral storage to set for the task\. The minimum supported value is `21` GiB and the maximum supported value is `200` GiB\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)