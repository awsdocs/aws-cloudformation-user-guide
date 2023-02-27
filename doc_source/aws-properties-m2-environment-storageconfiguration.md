# AWS::M2::Environment StorageConfiguration<a name="aws-properties-m2-environment-storageconfiguration"></a>

Defines the storage configuration for a runtime environment\.

## Syntax<a name="aws-properties-m2-environment-storageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-m2-environment-storageconfiguration-syntax.json"></a>

```
{
  "[Efs](#cfn-m2-environment-storageconfiguration-efs)" : EfsStorageConfiguration,
  "[Fsx](#cfn-m2-environment-storageconfiguration-fsx)" : FsxStorageConfiguration
}
```

### YAML<a name="aws-properties-m2-environment-storageconfiguration-syntax.yaml"></a>

```
  [Efs](#cfn-m2-environment-storageconfiguration-efs): 
    EfsStorageConfiguration
  [Fsx](#cfn-m2-environment-storageconfiguration-fsx): 
    FsxStorageConfiguration
```

## Properties<a name="aws-properties-m2-environment-storageconfiguration-properties"></a>

`Efs`  <a name="cfn-m2-environment-storageconfiguration-efs"></a>
Defines the storage configuration for an Amazon EFS file system\.  
*Required*: No  
*Type*: [EfsStorageConfiguration](aws-properties-m2-environment-efsstorageconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Fsx`  <a name="cfn-m2-environment-storageconfiguration-fsx"></a>
Defines the storage configuration for an Amazon FSx file system\.  
*Required*: No  
*Type*: [FsxStorageConfiguration](aws-properties-m2-environment-fsxstorageconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)