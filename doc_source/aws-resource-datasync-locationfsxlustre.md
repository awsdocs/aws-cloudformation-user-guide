# AWS::DataSync::LocationFSxLustre<a name="aws-resource-datasync-locationfsxlustre"></a>

The `AWS::DataSync::LocationFSxLustre` resource specifies an endpoint for an Amazon FSx for Lustre file system\.

## Syntax<a name="aws-resource-datasync-locationfsxlustre-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationfsxlustre-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationFSxLustre",
  "Properties" : {
      "[FsxFilesystemArn](#cfn-datasync-locationfsxlustre-fsxfilesystemarn)" : String,
      "[SecurityGroupArns](#cfn-datasync-locationfsxlustre-securitygrouparns)" : [ String, ... ],
      "[Subdirectory](#cfn-datasync-locationfsxlustre-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationfsxlustre-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-locationfsxlustre-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationFSxLustre
Properties: 
  [FsxFilesystemArn](#cfn-datasync-locationfsxlustre-fsxfilesystemarn): String
  [SecurityGroupArns](#cfn-datasync-locationfsxlustre-securitygrouparns): 
    - String
  [Subdirectory](#cfn-datasync-locationfsxlustre-subdirectory): String
  [Tags](#cfn-datasync-locationfsxlustre-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationfsxlustre-properties"></a>

`FsxFilesystemArn`  <a name="cfn-datasync-locationfsxlustre-fsxfilesystemarn"></a>
The Amazon Resource Name \(ARN\) for the FSx for Lustre file system\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):fsx:[a-z\-0-9]*:[0-9]{12}:file-system/fs-.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupArns`  <a name="cfn-datasync-locationfsxlustre-securitygrouparns"></a>
The ARNs of the security groups that are used to configure the FSx for Lustre file system\.  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):ec2:[a-z\-0-9]*:[0-9]{12}:security-group/.*$`  
*Length constraints*: Maximum length of 128\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationfsxlustre-subdirectory"></a>
A subdirectory in the location's path\. This subdirectory in the FSx for Lustre file system is used to read data from the FSx for Lustre source location or write data to the FSx for Lustre destination\.  
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\$\p{Zs}]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-locationfsxlustre-tags"></a>
The key\-value pair that represents a tag that you want to add to the resource\. The value can be an empty string\. This value helps you manage, filter, and search for your resources\. We recommend that you create a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationfsxlustre-return-values"></a>

### Ref<a name="aws-resource-datasync-locationfsxlustre-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationfsxlustre-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationfsxlustre-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The ARN of the specified FSx for Lustre file system location\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the specified FSx for Lustre file system location\.

## Examples<a name="aws-resource-datasync-locationfsxlustre--examples"></a>



### Specify an Amazon FSx for Lustre location for DataSync<a name="aws-resource-datasync-locationfsxlustre--examples--Specify_an_Amazon_FSx_for_Lustre_location_for_DataSync"></a>

The following examples specify an FSx for Lustre location for DataSync, including the subdirectory `/MySubdirectory`\.

#### JSON<a name="aws-resource-datasync-locationfsxlustre--examples--Specify_an_Amazon_FSx_for_Lustre_location_for_DataSync--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Specifies an FSx for Lustre location for DataSync",
    "Resources": {
        "LocationFSxLustre": {
            "Type": "AWS::DataSync::LocationFSxLustre",
            "Properties": {
                "FsxFilesystemArn": "arn:aws:fsx:us-east-2:111222333444:file-system/fs-12345fsx",
                "SecurityGroupArns": [
                    "arn:aws:ec2:us-east-2:11122233344:security-group/sg-12345678901212345"
                ],
                "Subdirectory": "/MySubdirectory"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-datasync-locationfsxlustre--examples--Specify_an_Amazon_FSx_for_Lustre_location_for_DataSync--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an FSx for Lustre location for DataSync
Resources:
  LocationFSxLustre:
    Type: AWS::DataSync::LocationFSxLustre
    Properties: 
      FsxFilesystemArn: arn:aws:fsx:us-east-2:111222333444:file-system/fs-12345fsx
      SecurityGroupArns: 
        - arn:aws:ec2:us-east-2:11122233344:security-group/sg-12345678901212345
      Subdirectory: /MySubdirectory
```