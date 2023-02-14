# AWS::Batch::JobDefinition EfsVolumeConfiguration<a name="aws-properties-batch-jobdefinition-efsvolumeconfiguration"></a>

This is used when you're using an Amazon Elastic File System file system for job storage\. For more information, see [Amazon EFS Volumes](https://docs.aws.amazon.com/batch/latest/userguide/efs-volumes.html) in the * AWS Batch User Guide*\.

## Syntax<a name="aws-properties-batch-jobdefinition-efsvolumeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-efsvolumeconfiguration-syntax.json"></a>

```
{
  "[AuthorizationConfig](#cfn-batch-jobdefinition-efsvolumeconfiguration-authorizationconfig)" : AuthorizationConfig,
  "[FileSystemId](#cfn-batch-jobdefinition-efsvolumeconfiguration-filesystemid)" : String,
  "[RootDirectory](#cfn-batch-jobdefinition-efsvolumeconfiguration-rootdirectory)" : String,
  "[TransitEncryption](#cfn-batch-jobdefinition-efsvolumeconfiguration-transitencryption)" : String,
  "[TransitEncryptionPort](#cfn-batch-jobdefinition-efsvolumeconfiguration-transitencryptionport)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobdefinition-efsvolumeconfiguration-syntax.yaml"></a>

```
  [AuthorizationConfig](#cfn-batch-jobdefinition-efsvolumeconfiguration-authorizationconfig): 
    AuthorizationConfig
  [FileSystemId](#cfn-batch-jobdefinition-efsvolumeconfiguration-filesystemid): String
  [RootDirectory](#cfn-batch-jobdefinition-efsvolumeconfiguration-rootdirectory): String
  [TransitEncryption](#cfn-batch-jobdefinition-efsvolumeconfiguration-transitencryption): String
  [TransitEncryptionPort](#cfn-batch-jobdefinition-efsvolumeconfiguration-transitencryptionport): Integer
```

## Properties<a name="aws-properties-batch-jobdefinition-efsvolumeconfiguration-properties"></a>

`AuthorizationConfig`  <a name="cfn-batch-jobdefinition-efsvolumeconfiguration-authorizationconfig"></a>
The authorization configuration details for the Amazon EFS file system\.  
*Required*: No  
*Type*: [AuthorizationConfig](aws-properties-batch-jobdefinition-authorizationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileSystemId`  <a name="cfn-batch-jobdefinition-efsvolumeconfiguration-filesystemid"></a>
The Amazon EFS file system ID to use\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RootDirectory`  <a name="cfn-batch-jobdefinition-efsvolumeconfiguration-rootdirectory"></a>
The directory within the Amazon EFS file system to mount as the root directory inside the host\. If this parameter is omitted, the root of the Amazon EFS volume is used instead\. Specifying `/` has the same effect as omitting this parameter\. The maximum length is 4,096 characters\.  
If an EFS access point is specified in the `authorizationConfig`, the root directory parameter must either be omitted or set to `/`, which enforces the path set on the Amazon EFS access point\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitEncryption`  <a name="cfn-batch-jobdefinition-efsvolumeconfiguration-transitencryption"></a>
Determines whether to enable encryption for Amazon EFS data in transit between the Amazon ECS host and the Amazon EFS server\. Transit encryption must be enabled if Amazon EFS IAM authorization is used\. If this parameter is omitted, the default value of `DISABLED` is used\. For more information, see [Encrypting data in transit](https://docs.aws.amazon.com/efs/latest/ug/encryption-in-transit.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TransitEncryptionPort`  <a name="cfn-batch-jobdefinition-efsvolumeconfiguration-transitencryptionport"></a>
The port to use when sending encrypted data between the Amazon ECS host and the Amazon EFS server\. If you don't specify a transit encryption port, it uses the port selection strategy that the Amazon EFS mount helper uses\. The value must be between 0 and 65,535\. For more information, see [EFS mount helper](https://docs.aws.amazon.com/efs/latest/ug/efs-mount-helper.html) in the *Amazon Elastic File System User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)