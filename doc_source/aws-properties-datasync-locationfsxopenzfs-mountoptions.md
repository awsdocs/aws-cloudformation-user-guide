# AWS::DataSync::LocationFSxOpenZFS MountOptions<a name="aws-properties-datasync-locationfsxopenzfs-mountoptions"></a>

Represents the mount options that are available for DataSync to access a Network File System \(NFS\) location\.

## Syntax<a name="aws-properties-datasync-locationfsxopenzfs-mountoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationfsxopenzfs-mountoptions-syntax.json"></a>

```
{
  "[Version](#cfn-datasync-locationfsxopenzfs-mountoptions-version)" : String
}
```

### YAML<a name="aws-properties-datasync-locationfsxopenzfs-mountoptions-syntax.yaml"></a>

```
  [Version](#cfn-datasync-locationfsxopenzfs-mountoptions-version): String
```

## Properties<a name="aws-properties-datasync-locationfsxopenzfs-mountoptions-properties"></a>

`Version`  <a name="cfn-datasync-locationfsxopenzfs-mountoptions-version"></a>
The specific NFS version that you want DataSync to use to mount your NFS share\. If the server refuses to use the version specified, the sync will fail\. If you don't specify a version, DataSync defaults to `AUTOMATIC`\. That is, DataSync automatically selects a version based on negotiation with the NFS server\.  
You can specify the following NFS versions:  
+ **[NFSv3](https://tools.ietf.org/html/rfc1813)**: Stateless protocol version that allows for asynchronous writes on the server\.
+ **[NFSv4\.0](https://tools.ietf.org/html/rfc3530)**: Stateful, firewall\-friendly protocol version that supports delegations and pseudo file systems\.
+ **[NFSv4\.1](https://tools.ietf.org/html/rfc5661)**: Stateful protocol version that supports sessions, directory delegations, and parallel data processing\. Version 4\.1 also includes all features available in version 4\.0\.
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | NFS3 | NFS4_0 | NFS4_1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)