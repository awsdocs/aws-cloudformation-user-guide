# AWS::ECS::TaskDefinition RuntimePlatform<a name="aws-properties-ecs-taskdefinition-runtimeplatform"></a>

Information about the platform for the Amazon ECS service or task\.

## Syntax<a name="aws-properties-ecs-taskdefinition-runtimeplatform-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-runtimeplatform-syntax.json"></a>

```
{
  "[CpuArchitecture](#cfn-ecs-taskdefinition-runtimeplatform-cpuarchitecture)" : String,
  "[OperatingSystemFamily](#cfn-ecs-taskdefinition-runtimeplatform-operatingsystemfamily)" : String
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-runtimeplatform-syntax.yaml"></a>

```
  [CpuArchitecture](#cfn-ecs-taskdefinition-runtimeplatform-cpuarchitecture): String
  [OperatingSystemFamily](#cfn-ecs-taskdefinition-runtimeplatform-operatingsystemfamily): String
```

## Properties<a name="aws-properties-ecs-taskdefinition-runtimeplatform-properties"></a>

`CpuArchitecture`  <a name="cfn-ecs-taskdefinition-runtimeplatform-cpuarchitecture"></a>
The CPU architecture\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ARM64 | X86_64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OperatingSystemFamily`  <a name="cfn-ecs-taskdefinition-runtimeplatform-operatingsystemfamily"></a>
The operating system\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LINUX | WINDOWS_SERVER_2004_CORE | WINDOWS_SERVER_2016_FULL | WINDOWS_SERVER_2019_CORE | WINDOWS_SERVER_2019_FULL | WINDOWS_SERVER_2022_CORE | WINDOWS_SERVER_2022_FULL | WINDOWS_SERVER_20H2_CORE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)