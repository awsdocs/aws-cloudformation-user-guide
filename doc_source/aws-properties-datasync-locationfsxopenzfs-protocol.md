# AWS::DataSync::LocationFSxOpenZFS Protocol<a name="aws-properties-datasync-locationfsxopenzfs-protocol"></a>

Represents the protocol that AWS DataSync uses to access your Amazon FSx for OpenZFS file system\.

## Syntax<a name="aws-properties-datasync-locationfsxopenzfs-protocol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationfsxopenzfs-protocol-syntax.json"></a>

```
{
  "[NFS](#cfn-datasync-locationfsxopenzfs-protocol-nfs)" : NFS
}
```

### YAML<a name="aws-properties-datasync-locationfsxopenzfs-protocol-syntax.yaml"></a>

```
  [NFS](#cfn-datasync-locationfsxopenzfs-protocol-nfs): 
    NFS
```

## Properties<a name="aws-properties-datasync-locationfsxopenzfs-protocol-properties"></a>

`NFS`  <a name="cfn-datasync-locationfsxopenzfs-protocol-nfs"></a>
Represents the Network File System \(NFS\) protocol that DataSync uses to access your FSx for OpenZFS file system\.  
*Required*: No  
*Type*: [NFS](aws-properties-datasync-locationfsxopenzfs-nfs.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)