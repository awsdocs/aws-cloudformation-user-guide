# AWS::ECS::TaskDefinition EFSVolumeConfiguration<a name="aws-properties-ecs-taskdefinition-efsvolumeconfiguration"></a>

This parameter is specified when you are using an Amazon Elastic File System file system for task storage\. For more information, see [Amazon EFS Volumes](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/efs-volumes.html) in the *Amazon Elastic Container Service Developer Guide*\.

## Syntax<a name="aws-properties-ecs-taskdefinition-efsvolumeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-taskdefinition-efsvolumeconfiguration-syntax.json"></a>

```
{
  "[AuthorizationConfig](#cfn-ecs-taskdefinition-efsvolumeconfiguration-authorizationconfig)" : AuthorizationConfig,
  "[FilesystemId](#cfn-ecs-taskdefinition-efsvolumeconfiguration-filesystemid)" : String,
  "[RootDirectory](#cfn-ecs-taskdefinition-efsvolumeconfiguration-rootdirectory)" : String,
  "[TransitEncryption](#cfn-ecs-taskdefinition-efsvolumeconfiguration-transitencryption)" : String,
  "[TransitEncryptionPort](#cfn-ecs-taskdefinition-efsvolumeconfiguration-transitencryptionport)" : Integer
}
```

### YAML<a name="aws-properties-ecs-taskdefinition-efsvolumeconfiguration-syntax.yaml"></a>

```
  [AuthorizationConfig](#cfn-ecs-taskdefinition-efsvolumeconfiguration-authorizationconfig): 
    AuthorizationConfig
  [FilesystemId](#cfn-ecs-taskdefinition-efsvolumeconfiguration-filesystemid): String
  [RootDirectory](#cfn-ecs-taskdefinition-efsvolumeconfiguration-rootdirectory): String
  [TransitEncryption](#cfn-ecs-taskdefinition-efsvolumeconfiguration-transitencryption): String
  [TransitEncryptionPort](#cfn-ecs-taskdefinition-efsvolumeconfiguration-transitencryptionport): Integer
```

## Properties<a name="aws-properties-ecs-taskdefinition-efsvolumeconfiguration-properties"></a>

`AuthorizationConfig`  <a name="cfn-ecs-taskdefinition-efsvolumeconfiguration-authorizationconfig"></a>
The authorization configuration details for the Amazon EFS file system\.  
*Required*: No  
*Type*: [AuthorizationConfig](aws-properties-ecs-taskdefinition-authorizationconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FilesystemId`  <a name="cfn-ecs-taskdefinition-efsvolumeconfiguration-filesystemid"></a>
The Amazon EFS file system ID to use\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RootDirectory`  <a name="cfn-ecs-taskdefinition-efsvolumeconfiguration-rootdirectory"></a>
The directory within the Amazon EFS file system to mount as the root directory inside the host\. If this parameter is omitted, the root of the Amazon EFS volume will be used\. Specifying `/` will have the same effect as omitting this parameter\.  
If an EFS access point is specified in the `authorizationConfig`, the root directory parameter must either be omitted or set to `/` which will enforce the path set on the EFS access point\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitEncryption`  <a name="cfn-ecs-taskdefinition-efsvolumeconfiguration-transitencryption"></a>
Whether or not to enable encryption for Amazon EFS data in transit between the Amazon ECS host and the Amazon EFS server\. Transit encryption must be enabled if Amazon EFS IAM authorization is used\. If this parameter is omitted, the default value of `DISABLED` is used\. For more information, see [Encrypting Data in Transit](https://docs.aws.amazon.com/efs/latest/ug/encryption-in-transit.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransitEncryptionPort`  <a name="cfn-ecs-taskdefinition-efsvolumeconfiguration-transitencryptionport"></a>
The port to use when sending encrypted data between the Amazon ECS host and the Amazon EFS server\. If you do not specify a transit encryption port, it will use the port selection strategy that the Amazon EFS mount helper uses\. For more information, see [EFS Mount Helper](https://docs.aws.amazon.com/efs/latest/ug/efs-mount-helper.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)