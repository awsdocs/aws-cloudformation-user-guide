# AWS::Batch::JobDefinition RuntimePlatform<a name="aws-properties-batch-jobdefinition-containerproperties-runtimeplatform"></a>

 An object that represents the compute environment architecture for AWS Batch jobs on Fargate\. 

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-runtimeplatform-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-runtimeplatform-syntax.json"></a>

```
{
  "[CpuArchitecture](#cfn-batch-jobdefinition-containerproperties-runtimeplatform-cpuarchitecture)" : String,
  "[OperatingSystemFamily](#cfn-batch-jobdefinition-containerproperties-runtimeplatform-operatingsystemfamily)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-runtimeplatform-syntax.yaml"></a>

```
  [CpuArchitecture](#cfn-batch-jobdefinition-containerproperties-runtimeplatform-cpuarchitecture): String
  [OperatingSystemFamily](#cfn-batch-jobdefinition-containerproperties-runtimeplatform-operatingsystemfamily): String
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-runtimeplatform-properties"></a>

`CpuArchitecture`  <a name="cfn-batch-jobdefinition-containerproperties-runtimeplatform-cpuarchitecture"></a>
 The vCPU architecture\. The default value is `X86_64`\. Valid values are `X86_64` and `ARM64`\.  
This parameter must be set to `X86_64` for Windows containers\.
Fargate Spot is not supported for `ARM64` and Windows\-based containers on Fargate\. A job queue will be blocked if a Fargate `ARM64` or Windows job is submitted to a job queue with only Fargate Spot compute environments\. However, you can attach both `FARGATE` and `FARGATE_SPOT` compute environments to the same job queue\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperatingSystemFamily`  <a name="cfn-batch-jobdefinition-containerproperties-runtimeplatform-operatingsystemfamily"></a>
The operating system for the compute environment\. Valid values are: `LINUX` \(default\), `WINDOWS_SERVER_2019_CORE`, `WINDOWS_SERVER_2019_FULL`, `WINDOWS_SERVER_2022_CORE`, and `WINDOWS_SERVER_2022_FULL`\.  
The following parameters can’t be set for Windows containers: `linuxParameters`, `privileged`, `user`, `ulimits`, `readonlyRootFilesystem`, and `efsVolumeConfiguration`\.
The AWS Batch Scheduler checks the compute environments that are attached to the job queue before registering a task definition with Fargate\. In this scenario, the job queue is where the job is submitted\. If the job requires a Windows container and the first compute environment is `LINUX`, the compute environment is skipped and the next compute environment is checked until a Windows\-based compute environment is found\.
Fargate Spot is not supported for `ARM64` and Windows\-based containers on Fargate\. A job queue will be blocked if a Fargate `ARM64` or Windows job is submitted to a job queue with only Fargate Spot compute environments\. However, you can attach both `FARGATE` and `FARGATE_SPOT` compute environments to the same job queue\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)