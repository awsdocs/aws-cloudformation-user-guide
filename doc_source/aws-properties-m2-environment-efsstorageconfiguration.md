# AWS::M2::Environment EfsStorageConfiguration<a name="aws-properties-m2-environment-efsstorageconfiguration"></a>

Defines the storage configuration for an Amazon EFS file system\.

## Syntax<a name="aws-properties-m2-environment-efsstorageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-m2-environment-efsstorageconfiguration-syntax.json"></a>

```
{
  "[FileSystemId](#cfn-m2-environment-efsstorageconfiguration-filesystemid)" : String,
  "[MountPoint](#cfn-m2-environment-efsstorageconfiguration-mountpoint)" : String
}
```

### YAML<a name="aws-properties-m2-environment-efsstorageconfiguration-syntax.yaml"></a>

```
  [FileSystemId](#cfn-m2-environment-efsstorageconfiguration-filesystemid): String
  [MountPoint](#cfn-m2-environment-efsstorageconfiguration-mountpoint): String
```

## Properties<a name="aws-properties-m2-environment-efsstorageconfiguration-properties"></a>

`FileSystemId`  <a name="cfn-m2-environment-efsstorageconfiguration-filesystemid"></a>
The file system identifier\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\S{1,200}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MountPoint`  <a name="cfn-m2-environment-efsstorageconfiguration-mountpoint"></a>
The mount point for the file system\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\S{1,200}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)