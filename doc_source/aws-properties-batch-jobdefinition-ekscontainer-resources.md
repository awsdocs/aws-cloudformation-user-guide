# AWS::Batch::JobDefinition Resources<a name="aws-properties-batch-jobdefinition-ekscontainer-resources"></a>

The type and quantity of the resources to request for the container\. The values vary based on the `name` that's specified\. Resources can be requested by using either the `limits` or the `requests` objects\.

memory  
The memory hard limit \(in MiB\) for the container, using whole integers, with a "Mi" suffix\. If your container attempts to exceed the memory specified, the container is terminated\. You must specify at least 4 MiB of memory for a job\. `memory` can be specified in `limits`, `requests`, or both\. If `memory` is specified in both, then the value that's specified in `limits` must be equal to the value that's specified in `requests`\.  
If you're trying to maximize your resource utilization by providing your jobs as much memory as possible for a particular instance type, see [Memory management](https://docs.aws.amazon.com/batch/latest/userguide/memory-management.html) in the * AWS Batch User Guide*\.

cpu  
The number of CPUs that are reserved for the container\. Values must be an even multiple of `0.25`\. `cpu` can be specified in `limits`, `requests`, or both\. If `cpu` is specified in both, then the value that's specified in `limits` must be at least as large as the value that's specified in `requests`\.

nvidia\.com/gpu  
The number of GPUs that are reserved for the container\. Values must be a whole integer\. `nvidia.com/gpu` can be specified in `limits`, `requests`, or both\. If `nvidia.com/gpu` is specified in both, then the value that's specified in `limits` must be equal to the value that's specified in `requests`\.

## Syntax<a name="aws-properties-batch-jobdefinition-ekscontainer-resources-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-ekscontainer-resources-syntax.json"></a>

```
{
  "[Limits](#cfn-batch-jobdefinition-ekscontainer-resources-limits)" : Json,
  "[Requests](#cfn-batch-jobdefinition-ekscontainer-resources-requests)" : Json
}
```

### YAML<a name="aws-properties-batch-jobdefinition-ekscontainer-resources-syntax.yaml"></a>

```
  [Limits](#cfn-batch-jobdefinition-ekscontainer-resources-limits): Json
  [Requests](#cfn-batch-jobdefinition-ekscontainer-resources-requests): Json
```

## Properties<a name="aws-properties-batch-jobdefinition-ekscontainer-resources-properties"></a>

`Limits`  <a name="cfn-batch-jobdefinition-ekscontainer-resources-limits"></a>
The type and quantity of the resources to reserve for the container\. The values vary based on the `name` that's specified\. Resources can be requested using either the `limits` or the `requests` objects\.    
memory  
The memory hard limit \(in MiB\) for the container, using whole integers, with a "Mi" suffix\. If your container attempts to exceed the memory specified, the container is terminated\. You must specify at least 4 MiB of memory for a job\. `memory` can be specified in `limits`, `requests`, or both\. If `memory` is specified in both places, then the value that's specified in `limits` must be equal to the value that's specified in `requests`\.  
To maximize your resource utilization, provide your jobs with as much memory as possible for the specific instance type that you are using\. To learn how, see [Memory management](https://docs.aws.amazon.com/batch/latest/userguide/memory-management.html) in the * AWS Batch User Guide*\.  
cpu  
The number of CPUs that's reserved for the container\. Values must be an even multiple of `0.25`\. `cpu` can be specified in `limits`, `requests`, or both\. If `cpu` is specified in both places, then the value that's specified in `limits` must be at least as large as the value that's specified in `requests`\.  
nvidia\.com/gpu  
The number of GPUs that's reserved for the container\. Values must be a whole integer\. `memory` can be specified in `limits`, `requests`, or both\. If `memory` is specified in both places, then the value that's specified in `limits` must be equal to the value that's specified in `requests`\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Requests`  <a name="cfn-batch-jobdefinition-ekscontainer-resources-requests"></a>
The type and quantity of the resources to request for the container\. The values vary based on the `name` that's specified\. Resources can be requested by using either the `limits` or the `requests` objects\.    
memory  
The memory hard limit \(in MiB\) for the container, using whole integers, with a "Mi" suffix\. If your container attempts to exceed the memory specified, the container is terminated\. You must specify at least 4 MiB of memory for a job\. `memory` can be specified in `limits`, `requests`, or both\. If `memory` is specified in both, then the value that's specified in `limits` must be equal to the value that's specified in `requests`\.  
If you're trying to maximize your resource utilization by providing your jobs as much memory as possible for a particular instance type, see [Memory management](https://docs.aws.amazon.com/batch/latest/userguide/memory-management.html) in the * AWS Batch User Guide*\.  
cpu  
The number of CPUs that are reserved for the container\. Values must be an even multiple of `0.25`\. `cpu` can be specified in `limits`, `requests`, or both\. If `cpu` is specified in both, then the value that's specified in `limits` must be at least as large as the value that's specified in `requests`\.  
nvidia\.com/gpu  
The number of GPUs that are reserved for the container\. Values must be a whole integer\. `nvidia.com/gpu` can be specified in `limits`, `requests`, or both\. If `nvidia.com/gpu` is specified in both, then the value that's specified in `limits` must be equal to the value that's specified in `requests`\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)