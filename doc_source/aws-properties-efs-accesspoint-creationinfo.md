# AWS::EFS::AccessPoint CreationInfo<a name="aws-properties-efs-accesspoint-creationinfo"></a>

Required if the `RootDirectory` > `Path` specified does not exist\. Specifies the POSIX IDs and permissions to apply to the access point's `RootDirectory` > `Path`\. If the access point root directory does not exist, EFS creates it with these settings when a client connects to the access point\. When specifying `CreationInfo`, you must include values for all properties\. 

Amazon EFS creates a root directory only if you have provided the CreationInfo: OwnUid, OwnGID, and permissions for the directory\. If you do not provide this information, Amazon EFS does not create the root directory\. If the root directory does not exist, attempts to mount using the access point will fail\.

**Important**  
If you do not provide `CreationInfo` and the specified `RootDirectory` does not exist, attempts to mount the file system using the access point will fail\.

## Syntax<a name="aws-properties-efs-accesspoint-creationinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-efs-accesspoint-creationinfo-syntax.json"></a>

```
{
  "[OwnerGid](#cfn-efs-accesspoint-creationinfo-ownergid)" : String,
  "[OwnerUid](#cfn-efs-accesspoint-creationinfo-owneruid)" : String,
  "[Permissions](#cfn-efs-accesspoint-creationinfo-permissions)" : String
}
```

### YAML<a name="aws-properties-efs-accesspoint-creationinfo-syntax.yaml"></a>

```
  [OwnerGid](#cfn-efs-accesspoint-creationinfo-ownergid): String
  [OwnerUid](#cfn-efs-accesspoint-creationinfo-owneruid): String
  [Permissions](#cfn-efs-accesspoint-creationinfo-permissions): String
```

## Properties<a name="aws-properties-efs-accesspoint-creationinfo-properties"></a>

`OwnerGid`  <a name="cfn-efs-accesspoint-creationinfo-ownergid"></a>
Specifies the POSIX group ID to apply to the `RootDirectory`\. Accepts values from 0 to 2^32 \(4294967295\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OwnerUid`  <a name="cfn-efs-accesspoint-creationinfo-owneruid"></a>
Specifies the POSIX user ID to apply to the `RootDirectory`\. Accepts values from 0 to 2^32 \(4294967295\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Permissions`  <a name="cfn-efs-accesspoint-creationinfo-permissions"></a>
Specifies the POSIX permissions to apply to the `RootDirectory`, in the format of an octal number representing the file's mode bits\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[0-7]{3,4}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)