# AWS::DataSync::LocationFSxONTAP SmbMountOptions<a name="aws-properties-datasync-locationfsxontap-smbmountoptions"></a>

Specifies the version of the Server Message Block \(SMB\) protocol that AWS DataSync uses to access an SMB file server\.

## Syntax<a name="aws-properties-datasync-locationfsxontap-smbmountoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationfsxontap-smbmountoptions-syntax.json"></a>

```
{
  "[Version](#cfn-datasync-locationfsxontap-smbmountoptions-version)" : String
}
```

### YAML<a name="aws-properties-datasync-locationfsxontap-smbmountoptions-syntax.yaml"></a>

```
  [Version](#cfn-datasync-locationfsxontap-smbmountoptions-version): String
```

## Properties<a name="aws-properties-datasync-locationfsxontap-smbmountoptions-properties"></a>

`Version`  <a name="cfn-datasync-locationfsxontap-smbmountoptions-version"></a>
By default, DataSync automatically chooses an SMB protocol version based on negotiation with your SMB file server\. You also can configure DataSync to use a specific SMB version, but we recommend doing this only if DataSync has trouble negotiating with the SMB file server automatically\.  
These are the following options for configuring the SMB version:  
+  `AUTOMATIC` \(default\): DataSync and the SMB file server negotiate the highest version of SMB that they mutually support between 2\.1 and 3\.1\.1\.

  This is the recommended option\. If you instead choose a specific version that your file server doesn't support, you may get an `Operation Not Supported` error\.
+  `SMB3`: Restricts the protocol negotiation to only SMB version 3\.0\.2\.
+  `SMB2`: Restricts the protocol negotiation to only SMB version 2\.1\.
+  `SMB2_0`: Restricts the protocol negotiation to only SMB version 2\.0\.
+  `SMB1`: Restricts the protocol negotiation to only SMB version 1\.0\.
**Note**  
The `SMB1` option isn't available when [creating an Amazon FSx for NetApp ONTAP location](https://docs.aws.amazon.com/datasync/latest/userguide/API_CreateLocationFsxOntap.html)\.
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | SMB1 | SMB2 | SMB2_0 | SMB3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)