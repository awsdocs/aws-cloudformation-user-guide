# AWS::Batch::JobDefinition ResourceRequirement<a name="aws-properties-batch-jobdefinition-resourcerequirement"></a>

The type and amount of a resource to assign to a container\. Currently, the only supported resource type is `GPU`\.

## Syntax<a name="aws-properties-batch-jobdefinition-resourcerequirement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-resourcerequirement-syntax.json"></a>

```
{
  "[Type](#cfn-batch-jobdefinition-resourcerequirement-type)" : String,
  "[Value](#cfn-batch-jobdefinition-resourcerequirement-value)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-resourcerequirement-syntax.yaml"></a>

```
  [Type](#cfn-batch-jobdefinition-resourcerequirement-type): String
  [Value](#cfn-batch-jobdefinition-resourcerequirement-value): String
```

## Properties<a name="aws-properties-batch-jobdefinition-resourcerequirement-properties"></a>

`Type`  <a name="cfn-batch-jobdefinition-resourcerequirement-type"></a>
The type of resource to assign to a container\. Currently, the only supported resource type is `GPU`\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `GPU`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-batch-jobdefinition-resourcerequirement-value"></a>
The number of physical GPUs to reserve for the container\. The number of GPUs reserved for all containers in a job should not exceed the number of available GPUs on the compute resource that the job is launched on\.  
*Required*: No  
*Type*: String  
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
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
