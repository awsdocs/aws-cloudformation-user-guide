# AWS::DataSync::LocationNFS MountOptions<a name="aws-properties-datasync-locationnfs-mountoptions"></a>

The NFS mount options that DataSync can use to mount your NFS share\.

## Syntax<a name="aws-properties-datasync-locationnfs-mountoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationnfs-mountoptions-syntax.json"></a>

```
{
  "[Version](#cfn-datasync-locationnfs-mountoptions-version)" : String
}
```

### YAML<a name="aws-properties-datasync-locationnfs-mountoptions-syntax.yaml"></a>

```
  [Version](#cfn-datasync-locationnfs-mountoptions-version): String
```

## Properties<a name="aws-properties-datasync-locationnfs-mountoptions-properties"></a>

`Version`  <a name="cfn-datasync-locationnfs-mountoptions-version"></a>
Specifies the NFS version that you want DataSync to use when mounting your NFS share\. If the server refuses to use the version specified, the task fails\.  
You can specify the following options:  
+  `AUTOMATIC` \(default\): DataSync chooses NFS version 4\.1\.
+  `NFS3`: Stateless protocol version that allows for asynchronous writes on the server\.
+  `NFSv4_0`: Stateful, firewall\-friendly protocol version that supports delegations and pseudo file systems\.
+  `NFSv4_1`: Stateful protocol version that supports sessions, directory delegations, and parallel data processing\. NFS version 4\.1 also includes all features available in version 4\.0\.
DataSync currently only supports NFS version 3 with Amazon FSx for NetApp ONTAP locations\.
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | NFS3 | NFS4_0 | NFS4_1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)