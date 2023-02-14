# AWS::FSx::FileSystem NfsExports<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports"></a>

The configuration object for mounting a file system\.

## Syntax<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-syntax.json"></a>

```
{
  "[ClientConfigurations](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations)" : [ ClientConfigurations, ... ]
}
```

### YAML<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-syntax.yaml"></a>

```
  [ClientConfigurations](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations): 
    - ClientConfigurations
```

## Properties<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-properties"></a>

`ClientConfigurations`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations"></a>
A list of configuration objects that contain the client and options for mounting the OpenZFS file system\.   
*Required*: No  
*Type*: [List](aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations.md) of [ClientConfigurations](aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations.md)  
*Maximum*: `25`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)