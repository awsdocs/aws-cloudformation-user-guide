# AWS::GreengrassV2::Deployment SystemResourceLimits<a name="aws-properties-greengrassv2-deployment-systemresourcelimits"></a>

Contains information about system resource limits that the software applies to a component's processes\.

## Syntax<a name="aws-properties-greengrassv2-deployment-systemresourcelimits-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-systemresourcelimits-syntax.json"></a>

```
{
  "[Cpus](#cfn-greengrassv2-deployment-systemresourcelimits-cpus)" : Double,
  "[Memory](#cfn-greengrassv2-deployment-systemresourcelimits-memory)" : Integer
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-systemresourcelimits-syntax.yaml"></a>

```
  [Cpus](#cfn-greengrassv2-deployment-systemresourcelimits-cpus): Double
  [Memory](#cfn-greengrassv2-deployment-systemresourcelimits-memory): Integer
```

## Properties<a name="aws-properties-greengrassv2-deployment-systemresourcelimits-properties"></a>

`Cpus`  <a name="cfn-greengrassv2-deployment-systemresourcelimits-cpus"></a>
The maximum amount of CPU time that a component's processes can use on the core device\. A core device's total CPU time is equivalent to the device's number of CPU cores\. For example, on a core device with 4 CPU cores, you can set this value to 2 to limit the component's processes to 50 percent usage of each CPU core\. On a device with 1 CPU core, you can set this value to 0\.25 to limit the component's processes to 25 percent usage of the CPU\. If you set this value to a number greater than the number of CPU cores, the AWS IoT Greengrass Core software doesn't limit the component's CPU usage\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Memory`  <a name="cfn-greengrassv2-deployment-systemresourcelimits-memory"></a>
The maximum amount of RAM, expressed in kilobytes, that a component's processes can use on the core device\. For more information, see [Configure system resource limits for components](https://docs.aws.amazon.com/greengrass/v2/developerguide/configure-greengrass-core-v2.html#configure-component-system-resource-limits)\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)