# AWS::DataSync::LocationFSxOpenZFS<a name="aws-resource-datasync-locationfsxopenzfs"></a>

The `AWS::DataSync::LocationFSxOpenZFS` resource specifies an endpoint for an Amazon FSx for OpenZFS file system\.

## Syntax<a name="aws-resource-datasync-locationfsxopenzfs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationfsxopenzfs-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationFSxOpenZFS",
  "Properties" : {
      "[FsxFilesystemArn](#cfn-datasync-locationfsxopenzfs-fsxfilesystemarn)" : String,
      "[Protocol](#cfn-datasync-locationfsxopenzfs-protocol)" : Protocol,
      "[SecurityGroupArns](#cfn-datasync-locationfsxopenzfs-securitygrouparns)" : [ String, ... ],
      "[Subdirectory](#cfn-datasync-locationfsxopenzfs-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationfsxopenzfs-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-locationfsxopenzfs-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationFSxOpenZFS
Properties: 
  [FsxFilesystemArn](#cfn-datasync-locationfsxopenzfs-fsxfilesystemarn): String
  [Protocol](#cfn-datasync-locationfsxopenzfs-protocol): 
    Protocol
  [SecurityGroupArns](#cfn-datasync-locationfsxopenzfs-securitygrouparns): 
    - String
  [Subdirectory](#cfn-datasync-locationfsxopenzfs-subdirectory): String
  [Tags](#cfn-datasync-locationfsxopenzfs-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationfsxopenzfs-properties"></a>

`FsxFilesystemArn`  <a name="cfn-datasync-locationfsxopenzfs-fsxfilesystemarn"></a>
The Amazon Resource Name \(ARN\) of the FSx for OpenZFS file system\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):fsx:[a-z\-0-9]*:[0-9]{12}:file-system/fs-.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-datasync-locationfsxopenzfs-protocol"></a>
The type of protocol that AWS DataSync uses to access your file system\.  
*Required*: Yes  
*Type*: [Protocol](aws-properties-datasync-locationfsxopenzfs-protocol.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupArns`  <a name="cfn-datasync-locationfsxopenzfs-securitygrouparns"></a>
The ARNs of the security groups that are used to configure the FSx for OpenZFS file system\.  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):ec2:[a-z\-0-9]*:[0-9]{12}:security-group/.*$`  
*Length constraints*: Maximum length of 128\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationfsxopenzfs-subdirectory"></a>
A subdirectory in the location's path that must begin with `/fsx`\. DataSync uses this subdirectory to read or write data \(depending on whether the file system is a source or destination location\)\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,4096}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-locationfsxopenzfs-tags"></a>
The key\-value pair that represents a tag that you want to add to the resource\. The value can be an empty string\. This value helps you manage, filter, and search for your resources\. We recommend that you create a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationfsxopenzfs-return-values"></a>

### Ref<a name="aws-resource-datasync-locationfsxopenzfs-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationfsxopenzfs-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationfsxopenzfs-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The ARN of the specified FSx for OpenZFS file system location\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the specified FSx for OpenZFS file system location\.

## Examples<a name="aws-resource-datasync-locationfsxopenzfs--examples"></a>



### Specify an Amazon FSx for OpenZFS location for DataSync<a name="aws-resource-datasync-locationfsxopenzfs--examples--Specify_an_Amazon_FSx_for_OpenZFS_location_for_DataSync"></a>

The following examples specify an FSx for OpenZFS location for DataSync\.

#### JSON<a name="aws-resource-datasync-locationfsxopenzfs--examples--Specify_an_Amazon_FSx_for_OpenZFS_location_for_DataSync--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Specifies an FSx for OpenZFS location for DataSync",
    "Resources": {
        "LocationFSxOpenZFS": {
            "Type": "AWS::DataSync::LocationFSxOpenZFS",
            "Properties": {
                "FsxFilesystemArn": "arn:aws:fsx:us-east-2:111222333444:file-system/fs-12345fsx",
                "Protocol": {
                    "NFS": {
                        "MountOptions": {
                            "Version": "NFS4_1"
                        }
                    }
                },
                "SecurityGroupArns": [
                    "arn:aws:ec2:us-east-2:11122233344:security-group/sg-12345678901212345"
                ],
                "Subdirectory": "/MySubdirectory"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-datasync-locationfsxopenzfs--examples--Specify_an_Amazon_FSx_for_OpenZFS_location_for_DataSync--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an FSx for OpenZFS location for DataSync
Resources:
  LocationFSxOpenZFS:
    Type: AWS::DataSync::LocationFSxOpenZFS
    Properties:
      FsxFilesystemArn: arn:aws:fsx:us-east-2:111222333444:file-system/fs-12345fsx
      Protocol:
        NFS:
          MountOptions:
            Version: NFS4_1
      SecurityGroupArns:
        - arn:aws:ec2:us-east-2:11122233344:security-group/sg-12345678901212345
      Subdirectory: /MySubdirectory
```