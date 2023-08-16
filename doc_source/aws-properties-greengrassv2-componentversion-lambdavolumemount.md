# AWS::GreengrassV2::ComponentVersion LambdaVolumeMount<a name="aws-properties-greengrassv2-componentversion-lambdavolumemount"></a>

Contains information about a volume that Linux processes in a container can access\. When you define a volume, the AWS IoT Greengrass Core software mounts the source files to the destination inside the container\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-lambdavolumemount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-lambdavolumemount-syntax.json"></a>

```
{
  "[AddGroupOwner](#cfn-greengrassv2-componentversion-lambdavolumemount-addgroupowner)" : Boolean,
  "[DestinationPath](#cfn-greengrassv2-componentversion-lambdavolumemount-destinationpath)" : String,
  "[Permission](#cfn-greengrassv2-componentversion-lambdavolumemount-permission)" : String,
  "[SourcePath](#cfn-greengrassv2-componentversion-lambdavolumemount-sourcepath)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-lambdavolumemount-syntax.yaml"></a>

```
  [AddGroupOwner](#cfn-greengrassv2-componentversion-lambdavolumemount-addgroupowner): Boolean
  [DestinationPath](#cfn-greengrassv2-componentversion-lambdavolumemount-destinationpath): String
  [Permission](#cfn-greengrassv2-componentversion-lambdavolumemount-permission): String
  [SourcePath](#cfn-greengrassv2-componentversion-lambdavolumemount-sourcepath): String
```

## Properties<a name="aws-properties-greengrassv2-componentversion-lambdavolumemount-properties"></a>

`AddGroupOwner`  <a name="cfn-greengrassv2-componentversion-lambdavolumemount-addgroupowner"></a>
Whether or not to add the AWS IoT Greengrass user group as an owner of the volume\.  
Default: `false`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationPath`  <a name="cfn-greengrassv2-componentversion-lambdavolumemount-destinationpath"></a>
The path to the logical volume in the file system\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Permission`  <a name="cfn-greengrassv2-componentversion-lambdavolumemount-permission"></a>
The permission to access the volume: read/only \(`ro`\) or read/write \(`rw`\)\.  
Default: `ro`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourcePath`  <a name="cfn-greengrassv2-componentversion-lambdavolumemount-sourcepath"></a>
The path to the physical volume in the file system\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)