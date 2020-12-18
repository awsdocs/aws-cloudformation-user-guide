# AWS::Batch::JobDefinition ResourceRequirement<a name="aws-properties-batch-jobdefinition-resourcerequirement"></a>

The type and amount of a resource to assign to a container\. The supported resources include `GPU`, `MEMORY`, and `VCPU`\.

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
The type of resource to assign to a container\. The supported resources include `GPU`, `MEMORY`, and `VCPU`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GPU | MEMORY | VCPU`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-batch-jobdefinition-resourcerequirement-value"></a>
The quantity of the specified resource to reserve for the container\. The values vary based on the `type` specified\.    
type="GPU"  
The number of physical GPUs to reserve for the container\. The number of GPUs reserved for all containers in a job shouldn't exceed the number of available GPUs on the compute resource that the job is launched on\.  
GPUs are not available for jobs running on Fargate resources\.  
type="MEMORY"  
For jobs running on EC2 resources, the hard limit \(in MiB\) of memory to present to the container\. If your container attempts to exceed the memory specified here, the container is killed\. This parameter maps to `Memory` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--memory` option to [docker run](https://docs.docker.com/engine/reference/run/)\. You must specify at least 4 MiB of memory for a job\. This is required but can be specified in several places for multi\-node parallel \(MNP\) jobs\. It must be specified for each node at least once\. This parameter maps to `Memory` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--memory` option to [docker run](https://docs.docker.com/engine/reference/run/)\. You must specify at least 4 MiB of memory for a job\.  
If you're trying to maximize your resource utilization by providing your jobs as much memory as possible for a particular instance type, see [Memory Management](https://docs.aws.amazon.com/batch/latest/userguide/memory-management.html) in the *AWS Batch User Guide*\.
For jobs running on Fargate resources, then `value` is the hard limit \(in GiB\), represented in decimal form, and must match one of the supported values \(0\.5 and whole numbers between 1 and 30, inclusive\) and the `VCPU` values must be one of the values supported for that memory value\.    
value = 0\.5  
 `VCPU` = 0\.25  
value = 1  
 `VCPU` = 0\.25 or 0\.5  
value = 2  
 `VCPU` = 0\.25, 0\.5, or 1  
value = 3  
 `VCPU` = 0\.5, or 1  
value = 4  
 `VCPU` = 0\.5, 1, or 2  
value = 5, 6, or 7  
 `VCPU` = 1 or 2  
value = 8  
 `VCPU` = 1, 2, or 4  
value = 9, 10, 11, 12, 13, 14, 15, or 16  
 `VCPU` = 2 or 4  
value = 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, or 30  
 `VCPU` = 4  
type="VCPU"  
The number of vCPUs reserved for the container\. This parameter maps to `CpuShares` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--cpu-shares` option to [docker run](https://docs.docker.com/engine/reference/run/)\. Each vCPU is equivalent to 1,024 CPU shares\. You must specify at least one vCPU\. This is required but can be specified in several places; it must be specified for each node at least once\.  
For jobs running on Fargate resources, then `value` must match one of the supported values and the `MEMORY` values must be one of the values supported for that VCPU value\. The supported values are 0\.25, 0\.5, 1, 2, and 4    
value = 0\.25  
 `MEMORY` = 0\.5, 1, or 2  
value = 0\.5  
 `MEMORY` = 1, 2, 3, or 4  
value = 1  
 `MEMORY` = 2, 3, 4, 5, 6, 7, or 8  
value = 2  
 `MEMORY` = 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, or 16  
value = 4  
 `MEMORY` = 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, or 30
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)