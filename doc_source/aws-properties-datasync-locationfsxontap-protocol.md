# AWS::DataSync::LocationFSxONTAP Protocol<a name="aws-properties-datasync-locationfsxontap-protocol"></a>

Specifies the data transfer protocol that AWS DataSync uses to access your Amazon FSx file system\.

## Syntax<a name="aws-properties-datasync-locationfsxontap-protocol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationfsxontap-protocol-syntax.json"></a>

```
{
  "[NFS](#cfn-datasync-locationfsxontap-protocol-nfs)" : NFS,
  "[SMB](#cfn-datasync-locationfsxontap-protocol-smb)" : SMB
}
```

### YAML<a name="aws-properties-datasync-locationfsxontap-protocol-syntax.yaml"></a>

```
  [NFS](#cfn-datasync-locationfsxontap-protocol-nfs): 
    NFS
  [SMB](#cfn-datasync-locationfsxontap-protocol-smb): 
    SMB
```

## Properties<a name="aws-properties-datasync-locationfsxontap-protocol-properties"></a>

`NFS`  <a name="cfn-datasync-locationfsxontap-protocol-nfs"></a>
Specifies the Network File System \(NFS\) protocol configuration that DataSync uses to access your FSx for ONTAP file system's storage virtual machine \(SVM\)\.  
*Required*: No  
*Type*: [NFS](aws-properties-datasync-locationfsxontap-nfs.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SMB`  <a name="cfn-datasync-locationfsxontap-protocol-smb"></a>
Specifies the Server Message Block \(SMB\) protocol configuration that DataSync uses to access your FSx for ONTAP file system's SVM\.  
*Required*: No  
*Type*: [SMB](aws-properties-datasync-locationfsxontap-smb.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)