# AWS::GreengrassV2::ComponentVersion LambdaContainerParams<a name="aws-properties-greengrassv2-componentversion-lambdacontainerparams"></a>

Contains information about a container in which AWS Lambda functions run on Greengrass core devices\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-lambdacontainerparams-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-lambdacontainerparams-syntax.json"></a>

```
{
  "[Devices](#cfn-greengrassv2-componentversion-lambdacontainerparams-devices)" : [ LambdaDeviceMount, ... ],
  "[MemorySizeInKB](#cfn-greengrassv2-componentversion-lambdacontainerparams-memorysizeinkb)" : Integer,
  "[MountROSysfs](#cfn-greengrassv2-componentversion-lambdacontainerparams-mountrosysfs)" : Boolean,
  "[Volumes](#cfn-greengrassv2-componentversion-lambdacontainerparams-volumes)" : [ LambdaVolumeMount, ... ]
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-lambdacontainerparams-syntax.yaml"></a>

```
  [Devices](#cfn-greengrassv2-componentversion-lambdacontainerparams-devices): 
    - LambdaDeviceMount
  [MemorySizeInKB](#cfn-greengrassv2-componentversion-lambdacontainerparams-memorysizeinkb): Integer
  [MountROSysfs](#cfn-greengrassv2-componentversion-lambdacontainerparams-mountrosysfs): Boolean
  [Volumes](#cfn-greengrassv2-componentversion-lambdacontainerparams-volumes): 
    - LambdaVolumeMount
```

## Properties<a name="aws-properties-greengrassv2-componentversion-lambdacontainerparams-properties"></a>

`Devices`  <a name="cfn-greengrassv2-componentversion-lambdacontainerparams-devices"></a>
The list of system devices that the container can access\.  
*Required*: No  
*Type*: List of [LambdaDeviceMount](aws-properties-greengrassv2-componentversion-lambdadevicemount.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MemorySizeInKB`  <a name="cfn-greengrassv2-componentversion-lambdacontainerparams-memorysizeinkb"></a>
The memory size of the container, expressed in kilobytes\.  
Default: `16384` \(16 MB\)  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MountROSysfs`  <a name="cfn-greengrassv2-componentversion-lambdacontainerparams-mountrosysfs"></a>
Whether or not the container can read information from the device's `/sys` folder\.  
Default: `false`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Volumes`  <a name="cfn-greengrassv2-componentversion-lambdacontainerparams-volumes"></a>
The list of volumes that the container can access\.  
*Required*: No  
*Type*: List of [LambdaVolumeMount](aws-properties-greengrassv2-componentversion-lambdavolumemount.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)