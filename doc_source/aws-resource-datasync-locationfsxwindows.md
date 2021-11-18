# AWS::DataSync::LocationFSxWindows<a name="aws-resource-datasync-locationfsxwindows"></a>

The `AWS::DataSync::LocationFSxWindows` resource specifies an endpoint for an Amazon FSx for Windows Server file system\.

## Syntax<a name="aws-resource-datasync-locationfsxwindows-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationfsxwindows-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationFSxWindows",
  "Properties" : {
      "[Domain](#cfn-datasync-locationfsxwindows-domain)" : String,
      "[FsxFilesystemArn](#cfn-datasync-locationfsxwindows-fsxfilesystemarn)" : String,
      "[Password](#cfn-datasync-locationfsxwindows-password)" : String,
      "[SecurityGroupArns](#cfn-datasync-locationfsxwindows-securitygrouparns)" : [ String, ... ],
      "[Subdirectory](#cfn-datasync-locationfsxwindows-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationfsxwindows-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[User](#cfn-datasync-locationfsxwindows-user)" : String
    }
}
```

### YAML<a name="aws-resource-datasync-locationfsxwindows-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationFSxWindows
Properties: 
  [Domain](#cfn-datasync-locationfsxwindows-domain): String
  [FsxFilesystemArn](#cfn-datasync-locationfsxwindows-fsxfilesystemarn): String
  [Password](#cfn-datasync-locationfsxwindows-password): String
  [SecurityGroupArns](#cfn-datasync-locationfsxwindows-securitygrouparns): 
    - String
  [Subdirectory](#cfn-datasync-locationfsxwindows-subdirectory): String
  [Tags](#cfn-datasync-locationfsxwindows-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [User](#cfn-datasync-locationfsxwindows-user): String
```

## Properties<a name="aws-resource-datasync-locationfsxwindows-properties"></a>

`Domain`  <a name="cfn-datasync-locationfsxwindows-domain"></a>
The name of the Windows domain that the FSx for Windows File Server belongs to\.  
*Required*: No  
*Type*: String  
*Maximum*: `253`  
*Pattern*: `^([A-Za-z0-9]+[A-Za-z0-9-.]*)*[A-Za-z0-9-]*[A-Za-z0-9]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FsxFilesystemArn`  <a name="cfn-datasync-locationfsxwindows-fsxfilesystemarn"></a>
The Amazon Resource Name \(ARN\) for the FSx for Windows File Server file system\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):fsx:[a-z\-0-9]*:[0-9]{12}:file-system/fs-.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Password`  <a name="cfn-datasync-locationfsxwindows-password"></a>
The password of the user who has the permissions to access files and folders in the FSx for Windows File Server file system\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `104`  
*Pattern*: `^.{0,104}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupArns`  <a name="cfn-datasync-locationfsxwindows-securitygrouparns"></a>
The Amazon Resource Names \(ARNs\) of the security groups that are used to configure the FSx for Windows File Server file system\.  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):ec2:[a-z\-0-9]*:[0-9]{12}:security-group/.*$`  
*Length Constraints*: Maximum length of 128\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationfsxwindows-subdirectory"></a>
A subdirectory in the location’s path\. This subdirectory in the Amazon FSx for Windows File Server file system is used to read data from the Amazon FSx for Windows File Server source location or write data to the FSx for Windows File Server destination\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\$\p{Zs}]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-locationfsxwindows-tags"></a>
The key\-value pair that represents a tag that you want to add to the resource\. The value can be an empty string\. This value helps you manage, filter, and search for your resources\. We recommend that you create a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`User`  <a name="cfn-datasync-locationfsxwindows-user"></a>
The user who has the permissions to access files and folders in the FSx for Windows File Server file system\.  
For information about choosing a user name that ensures sufficient permissions to files, folders, and metadata, see [user](https://docs.aws.amazon.com/datasync/latest/userguide/create-fsx-location.html#FSxWuser)\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `104`  
*Pattern*: `^[^\x5B\x5D\\/:;|=,+*?]{1,104}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-datasync-locationfsxwindows-return-values"></a>

### Ref<a name="aws-resource-datasync-locationfsxwindows-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationfsxwindows-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationfsxwindows-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the specified Amazon FSx for Windows Server file system location\. 

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the specified Amazon FSx for Windows Server file system\.

## Examples<a name="aws-resource-datasync-locationfsxwindows--examples"></a>



### Create an Amazon FSx for Windows File Server location for DataSync<a name="aws-resource-datasync-locationfsxwindows--examples--Create_an_Amazon_FSx_for_Windows_File_Server_location_for_DataSync"></a>

The following example specifies an FSx for Windows File Server location to be used by DataSync, with the subdirectory `/MySubdirectory`, user `Admin` and password\.

#### JSON<a name="aws-resource-datasync-locationfsxwindows--examples--Create_an_Amazon_FSx_for_Windows_File_Server_location_for_DataSync--json"></a>

```
{
"AWSTemplateFormatVersion": "2010-09-09",
"Description": "Specifies an FSx for Windows File Server location for DataSync",
"Resources": 
{
  "LocationFSxWindows": {
    "Type": "AWS::DataSync::LocationFSxWindows",
    "Properties": {
      "FsxFilesystemArn": "arn:aws:fsx:us-east-2:111222333444:file-system/fs-12345fsx",
      "SecurityGroupArns": [
        "arn:aws:ec2:us-east-2:11122233344:security-group/sg-0117195988293d62f"
      ],
      "Subdirectory": "/MySubdirectory",
      "User": "Admin",
      "Password": {"Ref": "Password"},
    }
  }
}
```

#### YAML<a name="aws-resource-datasync-locationfsxwindows--examples--Create_an_Amazon_FSx_for_Windows_File_Server_location_for_DataSync--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an FSx for Windows File Server location for DataSync
Resources:
  LocationFSxWindows:
    Type: AWS::DataSync::LocationFSxWindows
    Properties: 
      FsxFilesystemArn: arn:aws:fsx:us-east-2:111222333444:file-system/fs-12345fsx
      SecurityGroupArns: 
        - arn:aws:ec2:us-east-2:11122233344:security-group/sg-0117195988293d62f
      Subdirectory: /MySubdirectory
      User: Admin
      Password: !Ref Password
```