# AWS::EFS::AccessPoint<a name="aws-resource-efs-accesspoint"></a>

The `AWS::EFS::AccessPoint` resource creates an EFS access point\. An access point is an application\-specific view into an EFS file system that applies an operating system user and group, and a file system path, to any file system request made through the access point\. The operating system user and group override any identity information provided by the NFS client\. The file system path is exposed as the access point's root directory\. Applications using the access point can only access data in its own directory and below\. To learn more, see [Mounting a File System Using EFS Access Points](https://docs.aws.amazon.com/efs/latest/ug/efs-access-points.html)\.

This operation requires permissions for the `elasticfilesystem:CreateAccessPoint` action\.

## Syntax<a name="aws-resource-efs-accesspoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-efs-accesspoint-syntax.json"></a>

```
{
  "Type" : "AWS::EFS::AccessPoint",
  "Properties" : {
      "[AccessPointTags](#cfn-efs-accesspoint-accesspointtags)" : [ AccessPointTag, ... ],
      "[ClientToken](#cfn-efs-accesspoint-clienttoken)" : String,
      "[FileSystemId](#cfn-efs-accesspoint-filesystemid)" : String,
      "[PosixUser](#cfn-efs-accesspoint-posixuser)" : PosixUser,
      "[RootDirectory](#cfn-efs-accesspoint-rootdirectory)" : RootDirectory
    }
}
```

### YAML<a name="aws-resource-efs-accesspoint-syntax.yaml"></a>

```
Type: AWS::EFS::AccessPoint
Properties: 
  [AccessPointTags](#cfn-efs-accesspoint-accesspointtags): 
    - AccessPointTag
  [ClientToken](#cfn-efs-accesspoint-clienttoken): String
  [FileSystemId](#cfn-efs-accesspoint-filesystemid): String
  [PosixUser](#cfn-efs-accesspoint-posixuser): 
    PosixUser
  [RootDirectory](#cfn-efs-accesspoint-rootdirectory): 
    RootDirectory
```

## Properties<a name="aws-resource-efs-accesspoint-properties"></a>

`AccessPointTags`  <a name="cfn-efs-accesspoint-accesspointtags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [AccessPointTag](aws-properties-efs-accesspoint-accesspointtag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientToken`  <a name="cfn-efs-accesspoint-clienttoken"></a>
The opaque string specified in the request to ensure idempotent creation\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemId`  <a name="cfn-efs-accesspoint-filesystemid"></a>
The ID of the EFS file system that the access point applies to\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^(arn:aws[-a-z]*:elasticfilesystem:[0-9a-z-:]+:file-system/fs-[0-9a-f]{8,40}|fs-[0-9a-f]{8,40})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PosixUser`  <a name="cfn-efs-accesspoint-posixuser"></a>
The full POSIX identity, including the user ID, group ID, and secondary group IDs on the access point that is used for all file operations by NFS clients using the access point\.  
*Required*: No  
*Type*: [PosixUser](aws-properties-efs-accesspoint-posixuser.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RootDirectory`  <a name="cfn-efs-accesspoint-rootdirectory"></a>
The directory on the Amazon EFS file system that the access point exposes as the root directory to NFS clients using the access point\.  
*Required*: No  
*Type*: [RootDirectory](aws-properties-efs-accesspoint-rootdirectory.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-efs-accesspoint-return-values"></a>

### Ref<a name="aws-resource-efs-accesspoint-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID\. For example: 

 `{"Ref":"fsap-0123456789abcdef0"}`\.

 Ref returns the access point ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-efs-accesspoint-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-efs-accesspoint-return-values-fn--getatt-fn--getatt"></a>

`AccessPointId`  <a name="AccessPointId-fn::getatt"></a>
The ID of the EFS access point\.

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the access point\.

## Examples<a name="aws-resource-efs-accesspoint--examples"></a>



### Declare an Access Point for an EFS File System<a name="aws-resource-efs-accesspoint--examples--Declare_an_Access_Point_for_an_EFS_File_System"></a>

The following example declares an access point that is associated with an EFS file system\. For information about mounting file systems on EC2 instances, see [Mounting File Systems](https://docs.aws.amazon.com/efs/latest/ug/mounting-fs.html) in the *EFS User Guide*\.

#### JSON<a name="aws-resource-efs-accesspoint--examples--Declare_an_Access_Point_for_an_EFS_File_System--json"></a>

```
"AccessPointResource": {
            "Type": "AWS::EFS::AccessPoint",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FileSystemResource"
                },
                "PosixUser": {
                    "Uid": "13234",
                    "Gid": "1322",
                    "SecondaryGids": [
                        "1344",
                        "1452"
                    ]
                },
                "RootDirectory": {
                    "CreationInfo": {
                        "OwnerGid": "708798",
                        "OwnerUid": "7987987",
                        "Permissions": "0755"
                    },
                    "Path": "/testcfn/abc"
                }
            }
        }
}
```

#### YAML<a name="aws-resource-efs-accesspoint--examples--Declare_an_Access_Point_for_an_EFS_File_System--yaml"></a>

```
AccessPointResource:
    Type: 'AWS::EFS::AccessPoint'
    Properties:
      FileSystemId: !Ref FileSystemResource
      PosixUser:
        Uid: "13234"
        Gid: "1322"
        SecondaryGids:
          - "1344"
          - "1452"
      RootDirectory:
        CreationInfo:
          OwnerGid: "708798"
          OwnerUid: "7987987"
          Permissions: "0755"
        Path: "/testcfn/abc"
```

## See also<a name="aws-resource-efs-accesspoint--seealso"></a>
+ [Amazon EFS: How It Works](https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html)\.
+ [Working with Amazon EFS Access Points](https://docs.aws.amazon.com/efs/latest/ug/efs-access-points.html) in the *Amazon EFS User Guide*\.

