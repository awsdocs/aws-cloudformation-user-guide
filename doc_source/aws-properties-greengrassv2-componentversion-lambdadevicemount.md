# AWS::GreengrassV2::ComponentVersion LambdaDeviceMount<a name="aws-properties-greengrassv2-componentversion-lambdadevicemount"></a>

Contains information about a device that Linux processes in a container can access\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-lambdadevicemount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-lambdadevicemount-syntax.json"></a>

```
{
  "[AddGroupOwner](#cfn-greengrassv2-componentversion-lambdadevicemount-addgroupowner)" : Boolean,
  "[Path](#cfn-greengrassv2-componentversion-lambdadevicemount-path)" : String,
  "[Permission](#cfn-greengrassv2-componentversion-lambdadevicemount-permission)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-lambdadevicemount-syntax.yaml"></a>

```
  [AddGroupOwner](#cfn-greengrassv2-componentversion-lambdadevicemount-addgroupowner): Boolean
  [Path](#cfn-greengrassv2-componentversion-lambdadevicemount-path): String
  [Permission](#cfn-greengrassv2-componentversion-lambdadevicemount-permission): String
```

## Properties<a name="aws-properties-greengrassv2-componentversion-lambdadevicemount-properties"></a>

`AddGroupOwner`  <a name="cfn-greengrassv2-componentversion-lambdadevicemount-addgroupowner"></a>
Whether or not to add the component's system user as an owner of the device\.  
Default: `false`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Path`  <a name="cfn-greengrassv2-componentversion-lambdadevicemount-path"></a>
The mount path for the device in the file system\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Permission`  <a name="cfn-greengrassv2-componentversion-lambdadevicemount-permission"></a>
The permission to access the device: read/only \(`ro`\) or read/write \(`rw`\)\.  
Default: `ro`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)