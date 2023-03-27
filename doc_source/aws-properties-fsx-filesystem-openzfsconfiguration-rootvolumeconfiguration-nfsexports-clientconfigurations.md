# AWS::FSx::FileSystem ClientConfigurations<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations"></a>

Specifies who can mount an OpenZFS file system and the options available while mounting the file system\.

## Syntax<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-syntax.json"></a>

```
{
  "[Clients](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-clients)" : String,
  "[Options](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-options)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-syntax.yaml"></a>

```
  [Clients](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-clients): String
  [Options](#cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-options): 
    - String
```

## Properties<a name="aws-properties-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-properties"></a>

`Clients`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-clients"></a>
A value that specifies who can mount the file system\. You can provide a wildcard character \(`*`\), an IP address \(`0.0.0.0`\), or a CIDR address \(`192.0.2.0/24`\)\. By default, Amazon FSx uses the wildcard character when specifying the client\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[ -~]{1,128}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Options`  <a name="cfn-fsx-filesystem-openzfsconfiguration-rootvolumeconfiguration-nfsexports-clientconfigurations-options"></a>
The options to use when mounting the file system\. For a list of options that you can use with Network File System \(NFS\), see the [exports\(5\) \- Linux man page](https://linux.die.net/man/5/exports)\. When choosing your options, consider the following:  
+  `crossmnt` is used by default\. If you don't specify `crossmnt` when changing the client configuration, you won't be able to see or access snapshots in your file system's snapshot directory\.
+  `sync` is used by default\. If you instead specify `async`, the system acknowledges writes before writing to disk\. If the system crashes before the writes are finished, you lose the unwritten data\. 
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)