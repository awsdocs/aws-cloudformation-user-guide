# AWS::Pipes::Pipe EcsEphemeralStorage<a name="aws-properties-pipes-pipe-ecsephemeralstorage"></a>

The amount of ephemeral storage to allocate for the task\. This parameter is used to expand the total amount of ephemeral storage available, beyond the default amount, for tasks hosted on Fargate\. For more information, see [Fargate task storage](https://docs.aws.amazon.com/AmazonECS/latest/userguide/using_data_volumes.html) in the *Amazon ECS User Guide for Fargate*\.

**Note**  
This parameter is only supported for tasks hosted on Fargate using Linux platform version `1.4.0` or later\. This parameter is not supported for Windows containers on Fargate\.

## Syntax<a name="aws-properties-pipes-pipe-ecsephemeralstorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-ecsephemeralstorage-syntax.json"></a>

```
{
  "[SizeInGiB](#cfn-pipes-pipe-ecsephemeralstorage-sizeingib)" : Integer
}
```

### YAML<a name="aws-properties-pipes-pipe-ecsephemeralstorage-syntax.yaml"></a>

```
  [SizeInGiB](#cfn-pipes-pipe-ecsephemeralstorage-sizeingib): Integer
```

## Properties<a name="aws-properties-pipes-pipe-ecsephemeralstorage-properties"></a>

`SizeInGiB`  <a name="cfn-pipes-pipe-ecsephemeralstorage-sizeingib"></a>
The total amount, in GiB, of ephemeral storage to set for the task\. The minimum supported value is `21` GiB and the maximum supported value is `200` GiB\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)