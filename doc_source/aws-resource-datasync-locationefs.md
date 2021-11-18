# AWS::DataSync::LocationEFS<a name="aws-resource-datasync-locationefs"></a>

The `AWS::DataSync::LocationEFS` resource specifies an endpoint for an Amazon EFS location\.

## Syntax<a name="aws-resource-datasync-locationefs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationefs-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationEFS",
  "Properties" : {
      "[Ec2Config](#cfn-datasync-locationefs-ec2config)" : Ec2Config,
      "[EfsFilesystemArn](#cfn-datasync-locationefs-efsfilesystemarn)" : String,
      "[Subdirectory](#cfn-datasync-locationefs-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationefs-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-locationefs-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationEFS
Properties: 
  [Ec2Config](#cfn-datasync-locationefs-ec2config): 
    Ec2Config
  [EfsFilesystemArn](#cfn-datasync-locationefs-efsfilesystemarn): String
  [Subdirectory](#cfn-datasync-locationefs-subdirectory): String
  [Tags](#cfn-datasync-locationefs-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationefs-properties"></a>

`Ec2Config`  <a name="cfn-datasync-locationefs-ec2config"></a>
The subnet and security group that the Amazon EFS file system uses\. The security group that you provide needs to be able to communicate with the security group on the mount target in the subnet specified\.  
The exact relationship between security group M \(of the mount target\) and security group S \(which you provide for DataSync to use at this stage\) is as follows:   
+  Security group M \(which you associate with the mount target\) must allow inbound access for the Transmission Control Protocol \(TCP\) on the NFS port \(2049\) from security group S\. You can enable inbound connections either by IP address \(CIDR range\) or security group\. 
+ Security group S \(provided to DataSync to access EFS\) should have a rule that enables outbound connections to the NFS port on one of the file system’s mount targets\. You can enable outbound connections either by IP address \(CIDR range\) or security group\.

  For information about security groups and mount targets, see [Security Groups for Amazon EC2 Instances and Mount Targets](https://docs.aws.amazon.com/efs/latest/ug/security-considerations.html#network-access) in the *Amazon EFS User Guide\.* 
*Required*: Yes  
*Type*: [Ec2Config](aws-properties-datasync-locationefs-ec2config.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EfsFilesystemArn`  <a name="cfn-datasync-locationefs-efsfilesystemarn"></a>
The Amazon Resource Name \(ARN\) for the Amazon EFS file system\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):elasticfilesystem:[a-z\-0-9]*:[0-9]{12}:file-system/fs-.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationefs-subdirectory"></a>
A subdirectory in the location’s path\. This subdirectory in the EFS file system is used to read data from the EFS source location or write data to the EFS destination\. By default, AWS DataSync uses the root directory\.  
 `Subdirectory` must be specified with forward slashes\. For example, `/path/to/folder`\.
*Required*: No  
*Type*: String  
*Maximum*: `4096`  
*Pattern*: `^[a-zA-Z0-9_\-\+\./\(\)\p{Zs}]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-locationefs-tags"></a>
The key\-value pair that represents a tag that you want to add to the resource\. The value can be an empty string\. This value helps you manage, filter, and search for your resources\. We recommend that you create a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationefs-return-values"></a>

### Ref<a name="aws-resource-datasync-locationefs-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationefs-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationefs-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Amazon EFS file system\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the Amazon EFS file system\.

## Examples<a name="aws-resource-datasync-locationefs--examples"></a>



### Create an Amazon EFS location for DataSync<a name="aws-resource-datasync-locationefs--examples--Create_an_Amazon_EFS_location_for_DataSync"></a>

The following example specifies an EFS location to be used by DataSync, with the subdirectory `MySubdirectory`\.

#### JSON<a name="aws-resource-datasync-locationefs--examples--Create_an_Amazon_EFS_location_for_DataSync--json"></a>

```
{
"AWSTemplateFormatVersion": "2010-09-09",
"Description": "Specifies an EFS location for DataSync",
"Resources": 
  {
  "LocationEFS": {
    "Type": "AWS::DataSync::LocationEFS",
    "Properties": {
      "Ec2Config": {
      "SecurityGroupArns": [
        "arn:aws:ec2:us-east-2:11122233344:security-group/sg-0117195988293d62f"
        ],
        "SubnetArn": "arn:aws:ec2:us-east-2:11122233344:subnet/subnet-f45a0e678"
      },
      "EfsFilesystemArn": "arn:aws:elasticfilesystem:us-east-2:111222333444:file-system/fs-12345efs",
      "Subdirectory": "/MySubdirectory"
    }
  }
}
```

#### YAML<a name="aws-resource-datasync-locationefs--examples--Create_an_Amazon_EFS_location_for_DataSync--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies an EFS location for DataSync
Resources:
  LocationEFS:
    Type: AWS::DataSync::LocationEFS
      Properties: 
        Ec2Config: 
          SecurityGroupArns: 
            - arn:aws:ec2:us-east-2:11122233344:security-group/sg-0117195988293d62f
          SubnetArn: arn:aws:ec2:us-east-2:11122233344:subnet/subnet-f45a0e678
        EfsFilesystemArn: arn:aws:elasticfilesystem:us-east-2:111222333444:file-system/fs-12345efs
        Subdirectory: /MySubdirectory
```