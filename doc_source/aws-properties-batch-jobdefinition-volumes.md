# AWS::Batch::JobDefinition Volumes<a name="aws-properties-batch-jobdefinition-volumes"></a>

A list of volumes that are associated with the job\.

## Syntax<a name="aws-properties-batch-jobdefinition-volumes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-volumes-syntax.json"></a>

```
{
  "[EfsVolumeConfiguration](#cfn-batch-jobdefinition-volumes-efsvolumeconfiguration)" : EfsVolumeConfiguration,
  "[Host](#cfn-batch-jobdefinition-volumes-host)" : VolumesHost,
  "[Name](#cfn-batch-jobdefinition-volumes-name)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-volumes-syntax.yaml"></a>

```
  [EfsVolumeConfiguration](#cfn-batch-jobdefinition-volumes-efsvolumeconfiguration): 
    EfsVolumeConfiguration
  [Host](#cfn-batch-jobdefinition-volumes-host): 
    VolumesHost
  [Name](#cfn-batch-jobdefinition-volumes-name): String
```

## Properties<a name="aws-properties-batch-jobdefinition-volumes-properties"></a>

`EfsVolumeConfiguration`  <a name="cfn-batch-jobdefinition-volumes-efsvolumeconfiguration"></a>
This is used when you're using an Amazon Elastic File System file system for job storage\. For more information, see [Amazon EFS Volumes](https://docs.aws.amazon.com/batch/latest/userguide/efs-volumes.html) in the * AWS Batch User Guide*\.  
*Required*: No  
*Type*: [EfsVolumeConfiguration](aws-properties-batch-jobdefinition-efsvolumeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-batch-jobdefinition-volumes-host"></a>
The contents of the `host` parameter determine whether your data volume persists on the host container instance and where it's stored\. If the host parameter is empty, then the Docker daemon assigns a host path for your data volume\. However, the data isn't guaranteed to persist after the containers that are associated with it stop running\.  
This parameter isn't applicable to jobs that are running on Fargate resources and shouldn't be provided\.
*Required*: No  
*Type*: [VolumesHost](aws-properties-batch-jobdefinition-volumeshost.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-batch-jobdefinition-volumes-name"></a>
The name of the volume\. It can be up to 255 characters long\. It can contain uppercase and lowercase letters, numbers, hyphens \(\-\), and underscores \(\_\)\. This name is referenced in the `sourceVolume` parameter of container definition `mountPoints`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)