# AWS::Batch::JobDefinition EksContainerVolumeMount<a name="aws-properties-batch-jobdefinition-ekscontainervolumemount"></a>

The volume mounts for a container for an Amazon EKS job\. For more information about volumes and volume mounts in Kubernetes, see [Volumes](https://kubernetes.io/docs/concepts/storage/volumes/) in the *Kubernetes documentation*\.

## Syntax<a name="aws-properties-batch-jobdefinition-ekscontainervolumemount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-ekscontainervolumemount-syntax.json"></a>

```
{
  "[MountPath](#cfn-batch-jobdefinition-ekscontainervolumemount-mountpath)" : String,
  "[Name](#cfn-batch-jobdefinition-ekscontainervolumemount-name)" : String,
  "[ReadOnly](#cfn-batch-jobdefinition-ekscontainervolumemount-readonly)" : Boolean
}
```

### YAML<a name="aws-properties-batch-jobdefinition-ekscontainervolumemount-syntax.yaml"></a>

```
  [MountPath](#cfn-batch-jobdefinition-ekscontainervolumemount-mountpath): String
  [Name](#cfn-batch-jobdefinition-ekscontainervolumemount-name): String
  [ReadOnly](#cfn-batch-jobdefinition-ekscontainervolumemount-readonly): Boolean
```

## Properties<a name="aws-properties-batch-jobdefinition-ekscontainervolumemount-properties"></a>

`MountPath`  <a name="cfn-batch-jobdefinition-ekscontainervolumemount-mountpath"></a>
The path on the container where the volume is mounted\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-batch-jobdefinition-ekscontainervolumemount-name"></a>
The name the volume mount\. This must match the name of one of the volumes in the pod\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadOnly`  <a name="cfn-batch-jobdefinition-ekscontainervolumemount-readonly"></a>
If this value is `true`, the container has read\-only access to the volume\. Otherwise, the container can write to the volume\. The default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)