# AWS::DataSync::LocationFSxONTAP<a name="aws-resource-datasync-locationfsxontap"></a>

The `AWS::DataSync::LocationFSxONTAP` resource creates an endpoint for an Amazon FSx for NetApp ONTAP file system\. AWS DataSync can access this endpoint as a source or destination location\.

## Syntax<a name="aws-resource-datasync-locationfsxontap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-locationfsxontap-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::LocationFSxONTAP",
  "Properties" : {
      "[Protocol](#cfn-datasync-locationfsxontap-protocol)" : Protocol,
      "[SecurityGroupArns](#cfn-datasync-locationfsxontap-securitygrouparns)" : [ String, ... ],
      "[StorageVirtualMachineArn](#cfn-datasync-locationfsxontap-storagevirtualmachinearn)" : String,
      "[Subdirectory](#cfn-datasync-locationfsxontap-subdirectory)" : String,
      "[Tags](#cfn-datasync-locationfsxontap-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-datasync-locationfsxontap-syntax.yaml"></a>

```
Type: AWS::DataSync::LocationFSxONTAP
Properties: 
  [Protocol](#cfn-datasync-locationfsxontap-protocol): 
    Protocol
  [SecurityGroupArns](#cfn-datasync-locationfsxontap-securitygrouparns): 
    - String
  [StorageVirtualMachineArn](#cfn-datasync-locationfsxontap-storagevirtualmachinearn): String
  [Subdirectory](#cfn-datasync-locationfsxontap-subdirectory): String
  [Tags](#cfn-datasync-locationfsxontap-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-datasync-locationfsxontap-properties"></a>

`Protocol`  <a name="cfn-datasync-locationfsxontap-protocol"></a>
Specifies the data transfer protocol that DataSync uses to access your Amazon FSx file system\.  
*Required*: No  
*Type*: [Protocol](aws-properties-datasync-locationfsxontap-protocol.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupArns`  <a name="cfn-datasync-locationfsxontap-securitygrouparns"></a>
Specifies the Amazon Resource Names \(ARNs\) of the security groups that DataSync can use to access your FSx for ONTAP file system\. You must configure the security groups to allow outbound traffic on the following ports \(depending on the protocol that you're using\):  
+  **Network File System \(NFS\)**: TCP ports 111, 635, and 2049
+  **Server Message Block \(SMB\)**: TCP port 445
Your file system's security groups must also allow inbound traffic on the same port\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageVirtualMachineArn`  <a name="cfn-datasync-locationfsxontap-storagevirtualmachinearn"></a>
Specifies the ARN of the storage virtual machine \(SVM\) in your file system where you want to copy data to or from\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `162`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):fsx:[a-z\-0-9]+:[0-9]{12}:storage-virtual-machine/fs-[0-9a-f]+/svm-[0-9a-f]{17,}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subdirectory`  <a name="cfn-datasync-locationfsxontap-subdirectory"></a>
Specifies a path to the file share in the SVM where you'll copy your data\.  
You can specify a junction path \(also known as a mount point\), qtree path \(for NFS file shares\), or share name \(for SMB file shares\)\. For example, your mount path might be `/vol1`, `/vol1/tree1`, or `/share1`\.  
Don't specify a junction path in the SVM's root volume\. For more information, see [Managing FSx for ONTAP storage virtual machines](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/managing-svms.html) in the *Amazon FSx for NetApp ONTAP User Guide*\.
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,255}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-locationfsxontap-tags"></a>
Specifies labels that help you categorize, filter, and search for your AWS resources\. We recommend creating at least a name tag for your location\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-datasync-locationfsxontap-return-values"></a>

### Ref<a name="aws-resource-datasync-locationfsxontap-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the location resource ARN\. For example:

`arn:aws:datasync:us-east-2:111222333444:location/loc-07db7abfc326c50s3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-locationfsxontap-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-locationfsxontap-return-values-fn--getatt-fn--getatt"></a>

`FsxFilesystemArn`  <a name="FsxFilesystemArn-fn::getatt"></a>
The ARN of the FSx for ONTAP file system in the specified location\.

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
The ARN of the specified location\.

`LocationUri`  <a name="LocationUri-fn::getatt"></a>
The URI of the specified location\.

## Examples<a name="aws-resource-datasync-locationfsxontap--examples"></a>

### Creating an FSx for ONTAP location with NFS access<a name="aws-resource-datasync-locationfsxontap--examples--Creating_an_FSx_for_ONTAP_location_with_NFS_access"></a>

The following example creates a location for an FSx for ONTAP file system that DataSync can access using NFS\.

#### JSON<a name="aws-resource-datasync-locationfsxontap--examples--Creating_an_FSx_for_ONTAP_location_with_NFS_access--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Specifies a location for an Amazon FSx for ONTAP file system that DataSync can access using NFS.",
    "Resources": {
        "LocationFSxONTAP": {
            "Type": "AWS::DataSync::LocationFSxONTAP",
            "Properties": {
                "Protocol": {
                    "NFS": {
                        "MountOptions": {
                            "Version": "NFS3"
                        }
                    }
                },
                "SecurityGroupArns": [
                    "arn:aws:ec2:us-east-2:11122233344:security-group/sg-1234567890abcdef2"
                ],
                "StorageVirtualMachineArn": "arn:aws:fsx:us-east-1:11122233344:storage-virtual-machine/fs-abcdef01234567890/svm-021345abcdef6789",
                "Subdirectory": "/vol1"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-datasync-locationfsxontap--examples--Creating_an_FSx_for_ONTAP_location_with_NFS_access--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a location for an Amazon FSx for ONTAP file system that DataSync can access using NFS.
Resources:
  LocationFSxONTAP:
    Type: AWS::DataSync::LocationFSxONTAP
      Properties:
        Protocol:
          NFS:
            MountOptions:
              Version: NFS3
        SecurityGroupArns: 
          - arn:aws:ec2:us-east-2:11122233344:security-group/sg-1234567890abcdef2
        StorageVirtualMachineArn: arn:aws:fsx:us-east-1:11122233344:storage-virtual-machine/fs-abcdef01234567890/svm-021345abcdef6789
        Subdirectory: /vol1
```

### Creating an FSx for ONTAP location with SMB access<a name="aws-resource-datasync-locationfsxontap--examples--Creating_an_FSx_for_ONTAP_location_with_SMB_access"></a>

The following example creates a location for an FSx for ONTAP file system that DataSync can access using SMB\.

#### JSON<a name="aws-resource-datasync-locationfsxontap--examples--Creating_an_FSx_for_ONTAP_location_with_SMB_access--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Specifies a location for an Amazon FSx for ONTAP file system that DataSync can access using SMB.",
    "Resources": {
        "LocationFSxONTAP": {
            "Type": "AWS::DataSync::LocationFSxONTAP",
            "Properties": {
                "Protocol": {
                    "SMB": {
                        "Domain": "example.company",
                        "MountOptions": {
                            "Version": "AUTOMATIC"
                        },
                        "Password": "examplepassword",
                        "User": "exampleusername"
                    }
                },
                "SecurityGroupArns": [
                    "arn:aws:ec2:us-east-2:11122233344:security-group/sg-1234567890abcdef2"
                ],
                "StorageVirtualMachineArn": "arn:aws:fsx:us-east-1:11122233344:storage-virtual-machine/fs-abcdef01234567890/svm-021345abcdef6789",
                "Subdirectory": "/vol1"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-datasync-locationfsxontap--examples--Creating_an_FSx_for_ONTAP_location_with_SMB_access--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a location for an Amazon FSx for ONTAP file system that DataSync can access using SMB.
Resources:
  LocationFSxONTAP:
    Type: AWS::DataSync::LocationFSxONTAP
      Properties: 
        Protocol:
          SMB:
            Domain: example.company
            MountOptions:
              Version: AUTOMATIC
            Password: examplepassword
            User: exampleusername
        SecurityGroupArns: 
          - arn:aws:ec2:us-east-2:11122233344:security-group/sg-1234567890abcdef2
        StorageVirtualMachineArn: arn:aws:fsx:us-east-1:11122233344:storage-virtual-machine/fs-abcdef01234567890/svm-021345abcdef6789
        Subdirectory: /vol1
```