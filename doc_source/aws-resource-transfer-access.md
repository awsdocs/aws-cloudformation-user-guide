# AWS::Transfer::Access<a name="aws-resource-transfer-access"></a>

Used by administrators to choose which groups in the directory should have access to upload and download files over the enabled protocols using AWS Transfer Family\. For example, a Microsoft Active Directory might contain 50,000 users, but only a small fraction might need the ability to transfer files to the server\. An administrator can use `CreateAccess` to limit the access to the correct set of users who need this ability\.

## Syntax<a name="aws-resource-transfer-access-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-access-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Access",
  "Properties" : {
      "[ExternalId](#cfn-transfer-access-externalid)" : String,
      "[HomeDirectory](#cfn-transfer-access-homedirectory)" : String,
      "[HomeDirectoryMappings](#cfn-transfer-access-homedirectorymappings)" : [ HomeDirectoryMapEntry, ... ],
      "[HomeDirectoryType](#cfn-transfer-access-homedirectorytype)" : String,
      "[Policy](#cfn-transfer-access-policy)" : String,
      "[PosixProfile](#cfn-transfer-access-posixprofile)" : PosixProfile,
      "[Role](#cfn-transfer-access-role)" : String,
      "[ServerId](#cfn-transfer-access-serverid)" : String
    }
}
```

### YAML<a name="aws-resource-transfer-access-syntax.yaml"></a>

```
Type: AWS::Transfer::Access
Properties: 
  [ExternalId](#cfn-transfer-access-externalid): String
  [HomeDirectory](#cfn-transfer-access-homedirectory): String
  [HomeDirectoryMappings](#cfn-transfer-access-homedirectorymappings): 
    - HomeDirectoryMapEntry
  [HomeDirectoryType](#cfn-transfer-access-homedirectorytype): String
  [Policy](#cfn-transfer-access-policy): String
  [PosixProfile](#cfn-transfer-access-posixprofile): 
    PosixProfile
  [Role](#cfn-transfer-access-role): String
  [ServerId](#cfn-transfer-access-serverid): String
```

## Properties<a name="aws-resource-transfer-access-properties"></a>

`ExternalId`  <a name="cfn-transfer-access-externalid"></a>
A unique identifier that is required to identify specific groups within your directory\. The users of the group that you associate have access to your Amazon S3 or Amazon EFS resources over the enabled protocols using AWS Transfer Family\. If you know the group name, you can view the SID values by running the following command using Windows PowerShell\.  
 `Get-ADGroup -Filter {samAccountName -like "YourGroupName*"} -Properties * | Select SamAccountName,ObjectSid`   
In that command, replace *YourGroupName* with the name of your Active Directory group\.  
The regex used to validate this parameter is a string of characters consisting of uppercase and lowercase alphanumeric characters with no spaces\. You can also include underscores or any of the following characters: =,\.@:/\-  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^S-1-[\d-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HomeDirectory`  <a name="cfn-transfer-access-homedirectory"></a>
The landing directory \(folder\) for a user when they log in to the server using the client\.  
A `HomeDirectory` example is `/bucket_name/home/mydirectory`\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^$|/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HomeDirectoryMappings`  <a name="cfn-transfer-access-homedirectorymappings"></a>
Logical directory mappings that specify what Amazon S3 or Amazon EFS paths and keys should be visible to your user and how you want to make them visible\. You must specify the `Entry` and `Target` pair, where `Entry` shows how the path is made visible and `Target` is the actual Amazon S3 or Amazon EFS path\. If you only specify a target, it is displayed as is\. You also must ensure that your AWS Identity and Access Management \(IAM\) role provides access to paths in `Target`\. This value can only be set when `HomeDirectoryType` is set to *LOGICAL*\.  
In most cases, you can use this value instead of the scope\-down policy to lock down the associated access to the designated home directory \("`chroot`"\)\. To do this, you can set `Entry` to '/' and set `Target` to the `HomeDirectory` parameter value\.  
*Required*: No  
*Type*: List of [HomeDirectoryMapEntry](aws-properties-transfer-access-homedirectorymapentry.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HomeDirectoryType`  <a name="cfn-transfer-access-homedirectorytype"></a>
The type of landing directory \(folder\) you want your users' home directory to be when they log into the server\. If you set it to `PATH`, the user will see the absolute Amazon S3 bucket or EFS paths as is in their file transfer protocol clients\. If you set it `LOGICAL`, you will need to provide mappings in the `HomeDirectoryMappings` for how you want to make Amazon S3 or EFS paths visible to your users\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LOGICAL | PATH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policy`  <a name="cfn-transfer-access-policy"></a>
A scope\-down policy for your user so that you can use the same IAM role across multiple users\. This policy scopes down user access to portions of their Amazon S3 bucket\. Variables that you can use inside this policy include `${Transfer:UserName}`, `${Transfer:HomeDirectory}`, and `${Transfer:HomeBucket}`\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PosixProfile`  <a name="cfn-transfer-access-posixprofile"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [PosixProfile](aws-properties-transfer-access-posixprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-transfer-access-role"></a>
Specifies the Amazon Resource Name \(ARN\) of the IAM role that controls your users' access to your Amazon S3 bucket or EFS file system\. The policies attached to this role determine the level of access that you want to provide your users when transferring files into and out of your Amazon S3 bucket or EFS file system\. The IAM role should also contain a trust relationship that allows the server to access your resources when servicing your users' transfer requests\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerId`  <a name="cfn-transfer-access-serverid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-transfer-access-return-values"></a>

### Ref<a name="aws-resource-transfer-access-return-values-ref"></a>