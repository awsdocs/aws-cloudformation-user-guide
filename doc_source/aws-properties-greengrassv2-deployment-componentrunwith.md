# AWS::GreengrassV2::Deployment ComponentRunWith<a name="aws-properties-greengrassv2-deployment-componentrunwith"></a>

Contains information system user and group that the AWS IoT Greengrass Core software uses to run component processes on the core device\. For more information, see [Configure the user and group that run components](https://docs.aws.amazon.com/greengrass/v2/developerguide/configure-greengrass-core-v2.html#configure-component-user) in the *AWS IoT Greengrass V2 Developer Guide*\.

## Syntax<a name="aws-properties-greengrassv2-deployment-componentrunwith-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-deployment-componentrunwith-syntax.json"></a>

```
{
  "[PosixUser](#cfn-greengrassv2-deployment-componentrunwith-posixuser)" : String,
  "[SystemResourceLimits](#cfn-greengrassv2-deployment-componentrunwith-systemresourcelimits)" : SystemResourceLimits,
  "[WindowsUser](#cfn-greengrassv2-deployment-componentrunwith-windowsuser)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-deployment-componentrunwith-syntax.yaml"></a>

```
  [PosixUser](#cfn-greengrassv2-deployment-componentrunwith-posixuser): String
  [SystemResourceLimits](#cfn-greengrassv2-deployment-componentrunwith-systemresourcelimits): 
    SystemResourceLimits
  [WindowsUser](#cfn-greengrassv2-deployment-componentrunwith-windowsuser): String
```

## Properties<a name="aws-properties-greengrassv2-deployment-componentrunwith-properties"></a>

`PosixUser`  <a name="cfn-greengrassv2-deployment-componentrunwith-posixuser"></a>
The POSIX system user and \(optional\) group to use to run this component\. Specify the user and group separated by a colon \(`:`\) in the following format: `user:group`\. The group is optional\. If you don't specify a group, the AWS IoT Greengrass Core software uses the primary user for the group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SystemResourceLimits`  <a name="cfn-greengrassv2-deployment-componentrunwith-systemresourcelimits"></a>
The system resource limits to apply to this component's process on the core device\. AWS IoT Greengrass supports this feature only on Linux core devices\.  
If you omit this parameter, the AWS IoT Greengrass Core software uses the default system resource limits that you configure on the AWS IoT Greengrass nucleus component\. For more information, see [ Configure system resource limits for components ](https://docs.aws.amazon.com/greengrass/v2/developerguide/configure-greengrass-core-v2.html#configure-component-system-resource-limits)\.  
*Required*: No  
*Type*: [SystemResourceLimits](aws-properties-greengrassv2-deployment-systemresourcelimits.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WindowsUser`  <a name="cfn-greengrassv2-deployment-componentrunwith-windowsuser"></a>
The Windows user to use to run this component on Windows core devices\. The user must exist on each Windows core device, and its name and password must be in the LocalSystem account's Credentials Manager instance\.  
If you omit this parameter, the AWS IoT Greengrass Core software uses the default Windows user that you configure on the AWS IoT Greengrass nucleus component\. For more information, see [Configure the user and group that run components](https://docs.aws.amazon.com/greengrass/v2/developerguide/configure-greengrass-core-v2.html#configure-component-user)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)