# AWS::FSx::Volume NfsExports<a name="aws-properties-fsx-volume-openzfsconfiguration-nfsexports"></a>

The configuration object for mounting a Network File System \(NFS\) file system\.

## Syntax<a name="aws-properties-fsx-volume-openzfsconfiguration-nfsexports-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-openzfsconfiguration-nfsexports-syntax.json"></a>

```
{
  "[ClientConfigurations](#cfn-fsx-volume-openzfsconfiguration-nfsexports-clientconfigurations)" : [ ClientConfigurations, ... ]
}
```

### YAML<a name="aws-properties-fsx-volume-openzfsconfiguration-nfsexports-syntax.yaml"></a>

```
  [ClientConfigurations](#cfn-fsx-volume-openzfsconfiguration-nfsexports-clientconfigurations): 
    - ClientConfigurations
```

## Properties<a name="aws-properties-fsx-volume-openzfsconfiguration-nfsexports-properties"></a>

`ClientConfigurations`  <a name="cfn-fsx-volume-openzfsconfiguration-nfsexports-clientconfigurations"></a>
A list of configuration objects that contain the client and options for mounting the OpenZFS file system\.   
*Required*: Yes  
*Type*: [List](aws-properties-fsx-volume-openzfsconfiguration-nfsexports-clientconfigurations.md) of [ClientConfigurations](aws-properties-fsx-volume-openzfsconfiguration-nfsexports-clientconfigurations.md)  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)