# AWS::Batch::JobDefinition Device<a name="aws-properties-batch-jobdefinition-device"></a>

An object representing a container instance host device\.

**Note**  
This object isn't applicable to jobs running on Fargate resources and shouldn't be provided\.

## Syntax<a name="aws-properties-batch-jobdefinition-device-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-device-syntax.json"></a>

```
{
  "[ContainerPath](#cfn-batch-jobdefinition-device-containerpath)" : String,
  "[HostPath](#cfn-batch-jobdefinition-device-hostpath)" : String,
  "[Permissions](#cfn-batch-jobdefinition-device-permissions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-device-syntax.yaml"></a>

```
  [ContainerPath](#cfn-batch-jobdefinition-device-containerpath): String
  [HostPath](#cfn-batch-jobdefinition-device-hostpath): String
  [Permissions](#cfn-batch-jobdefinition-device-permissions): 
    - String
```

## Properties<a name="aws-properties-batch-jobdefinition-device-properties"></a>

`ContainerPath`  <a name="cfn-batch-jobdefinition-device-containerpath"></a>
The path inside the container used to expose the host device\. By default the `hostPath` value is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostPath`  <a name="cfn-batch-jobdefinition-device-hostpath"></a>
The path for the device on the host container instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-batch-jobdefinition-device-permissions"></a>
The explicit permissions to provide to the container for the device\. By default, the container has permissions for `read`, `write`, and `mknod` for the device\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)