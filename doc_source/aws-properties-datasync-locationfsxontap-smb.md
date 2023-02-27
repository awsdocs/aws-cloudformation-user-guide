# AWS::DataSync::LocationFSxONTAP SMB<a name="aws-properties-datasync-locationfsxontap-smb"></a>

Specifies the Server Message Block \(SMB\) protocol configuration that AWS DataSync uses to access a storage virtual machine \(SVM\) on your Amazon FSx for NetApp ONTAP file system\. For more information, see [Accessing FSx for ONTAP file systems](https://docs.aws.amazon.com/datasync/latest/userguide/create-ontap-location.html#create-ontap-location-access)\.

## Syntax<a name="aws-properties-datasync-locationfsxontap-smb-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationfsxontap-smb-syntax.json"></a>

```
{
  "[Domain](#cfn-datasync-locationfsxontap-smb-domain)" : String,
  "[MountOptions](#cfn-datasync-locationfsxontap-smb-mountoptions)" : SmbMountOptions,
  "[Password](#cfn-datasync-locationfsxontap-smb-password)" : String,
  "[User](#cfn-datasync-locationfsxontap-smb-user)" : String
}
```

### YAML<a name="aws-properties-datasync-locationfsxontap-smb-syntax.yaml"></a>

```
  [Domain](#cfn-datasync-locationfsxontap-smb-domain): String
  [MountOptions](#cfn-datasync-locationfsxontap-smb-mountoptions): 
    SmbMountOptions
  [Password](#cfn-datasync-locationfsxontap-smb-password): String
  [User](#cfn-datasync-locationfsxontap-smb-user): String
```

## Properties<a name="aws-properties-datasync-locationfsxontap-smb-properties"></a>

`Domain`  <a name="cfn-datasync-locationfsxontap-smb-domain"></a>
Specifies the fully qualified domain name \(FQDN\) of the Microsoft Active Directory that your storage virtual machine \(SVM\) belongs to\.  
*Required*: No  
*Type*: String  
*Maximum*: `253`  
*Pattern*: `^[A-Za-z0-9]((\.|-+)?[A-Za-z0-9]){0,252}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MountOptions`  <a name="cfn-datasync-locationfsxontap-smb-mountoptions"></a>
Specifies how DataSync can access a location using the SMB protocol\.  
*Required*: Yes  
*Type*: [SmbMountOptions](aws-properties-datasync-locationfsxontap-smbmountoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Password`  <a name="cfn-datasync-locationfsxontap-smb-password"></a>
Specifies the password of a user who has permission to access your SVM\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `104`  
*Pattern*: `^.{0,104}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`User`  <a name="cfn-datasync-locationfsxontap-smb-user"></a>
Specifies a user name that can mount the location and access the files, folders, and metadata that you need in the SVM\.  
If you provide a user in your Active Directory, note the following:  
+ If you're using AWS Directory Service for Microsoft Active Directory, the user must be a member of the AWS Delegated FSx Administrators group\.
+  If you're using a self\-managed Active Directory, the user must be a member of either the Domain Admins group or a custom group that you specified for file system administration when you created your file system\.
Make sure that the user has the permissions it needs to copy the data you want:  
+ `SE_TCB_NAME`: Required to set object ownership and file metadata\. With this privilege, you also can copy NTFS discretionary access lists \(DACLs\)\.
+ `SE_SECURITY_NAME`: May be needed to copy NTFS system access control lists \(SACLs\)\. This operation specifically requires the Windows privilege, which is granted to members of the Domain Admins group\. If you configure your task to copy SACLs, make sure that the user has the required privileges\. For information about copying SACLs, see [Ownership and permissions\-related options](https://docs.aws.amazon.com/datasync/latest/userguide/create-task.html#configure-ownership-and-permissions)\.
*Required*: Yes  
*Type*: String  
*Maximum*: `104`  
*Pattern*: `^[^\x5B\x5D\\/:;|=,+*?]{1,104}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)