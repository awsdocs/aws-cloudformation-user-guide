# AWS::EFS::AccessPoint PosixUser<a name="aws-properties-efs-accesspoint-posixuser"></a>

The full POSIX identity, including the user ID, group ID, and any secondary group IDs, on the access point that is used for all file system operations performed by NFS clients using the access point\.

## Syntax<a name="aws-properties-efs-accesspoint-posixuser-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-efs-accesspoint-posixuser-syntax.json"></a>

```
{
  "[Gid](#cfn-efs-accesspoint-posixuser-gid)" : String,
  "[SecondaryGids](#cfn-efs-accesspoint-posixuser-secondarygids)" : [ String, ... ],
  "[Uid](#cfn-efs-accesspoint-posixuser-uid)" : String
}
```

### YAML<a name="aws-properties-efs-accesspoint-posixuser-syntax.yaml"></a>

```
  [Gid](#cfn-efs-accesspoint-posixuser-gid): String
  [SecondaryGids](#cfn-efs-accesspoint-posixuser-secondarygids): 
    - String
  [Uid](#cfn-efs-accesspoint-posixuser-uid): String
```

## Properties<a name="aws-properties-efs-accesspoint-posixuser-properties"></a>

`Gid`  <a name="cfn-efs-accesspoint-posixuser-gid"></a>
The POSIX group ID used for all file system operations using this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecondaryGids`  <a name="cfn-efs-accesspoint-posixuser-secondarygids"></a>
Secondary POSIX group IDs used for all file system operations using this access point\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Uid`  <a name="cfn-efs-accesspoint-posixuser-uid"></a>
The POSIX user ID used for all file system operations using this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)