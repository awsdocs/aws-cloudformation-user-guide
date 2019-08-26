# AWS::FSx::FileSystem<a name="aws-resource-fsx-filesystem"></a>

The `AWS::FSx::FileSystem` resource is an Amazon FSx resource type that creates either an Amazon FSx for Windows File Server file system or an Amazon FSx for Lustre file system\.

## Syntax<a name="aws-resource-fsx-filesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fsx-filesystem-syntax.json"></a>

```
{
  "Type" : "AWS::FSx::FileSystem",
  "Properties" : {
      "[BackupId](#cfn-fsx-filesystem-backupid)" : String,
      "[FileSystemType](#cfn-fsx-filesystem-filesystemtype)" : String,
      "[KmsKeyId](#cfn-fsx-filesystem-kmskeyid)" : String,
      "[LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration)" : [LustreConfiguration](aws-properties-fsx-filesystem-lustreconfiguration.md),
      "[SecurityGroupIds](#cfn-fsx-filesystem-securitygroupids)" : [ String, ... ],
      "[StorageCapacity](#cfn-fsx-filesystem-storagecapacity)" : Integer,
      "[SubnetIds](#cfn-fsx-filesystem-subnetids)" : [ String, ... ],
      "[Tags](#cfn-fsx-filesystem-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WindowsConfiguration](#cfn-fsx-filesystem-windowsconfiguration)" : [WindowsConfiguration](aws-properties-fsx-filesystem-windowsconfiguration.md)
    }
}
```

### YAML<a name="aws-resource-fsx-filesystem-syntax.yaml"></a>

```
Type: AWS::FSx::FileSystem
Properties: 
  [BackupId](#cfn-fsx-filesystem-backupid): String
  [FileSystemType](#cfn-fsx-filesystem-filesystemtype): String
  [KmsKeyId](#cfn-fsx-filesystem-kmskeyid): String
  [LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration): 
    [LustreConfiguration](aws-properties-fsx-filesystem-lustreconfiguration.md)
  [SecurityGroupIds](#cfn-fsx-filesystem-securitygroupids): 
    - String
  [StorageCapacity](#cfn-fsx-filesystem-storagecapacity): Integer
  [SubnetIds](#cfn-fsx-filesystem-subnetids): 
    - String
  [Tags](#cfn-fsx-filesystem-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WindowsConfiguration](#cfn-fsx-filesystem-windowsconfiguration): 
    [WindowsConfiguration](aws-properties-fsx-filesystem-windowsconfiguration.md)
```

## Properties<a name="aws-resource-fsx-filesystem-properties"></a>

`BackupId`  <a name="cfn-fsx-filesystem-backupid"></a>
The ID of the backup\. Specifies the backup to use if you're creating a file system from an existing backup\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemType`  <a name="cfn-fsx-filesystem-filesystemtype"></a>
Type of file system\. Currently the only supported type is WINDOWS\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `LUSTRE | WINDOWS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-fsx-filesystem-kmskeyid"></a>
The ID of the AWS Key Management Service \(AWS KMS\) key used to encrypt the file system's data for an Amazon FSx for Windows File Server file system\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LustreConfiguration`  <a name="cfn-fsx-filesystem-lustreconfiguration"></a>
The configuration object for Lustre file systems used in the `CreateFileSystem` operation\.  
*Required*: No  
*Type*: [LustreConfiguration](aws-properties-fsx-filesystem-lustreconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-fsx-filesystem-securitygroupids"></a>
A list of IDs for the security groups that apply to the specified network interfaces created for file system access\. These security groups will apply to all network interfaces\. This list isn't returned in later describe requests\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageCapacity`  <a name="cfn-fsx-filesystem-storagecapacity"></a>
The storage capacity of the file system\.  
For Windows file systems, the storage capacity has a minimum of 300 GiB, and a maximum of 65,536 GiB\.  
For Lustre file systems, the storage capacity has a minimum of 3,600 GiB\. Storage capacity is provisioned in increments of 3,600 GiB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-fsx-filesystem-subnetids"></a>
The IDs of the subnets to contain the endpoint for the file system\. One and only one is supported\. The file system is launched in the Availability Zone associated with this subnet\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-fsx-filesystem-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowsConfiguration`  <a name="cfn-fsx-filesystem-windowsconfiguration"></a>
The configuration object for the Microsoft Windows file system you are creating\.   
*Required*: No  
*Type*: [WindowsConfiguration](aws-properties-fsx-filesystem-windowsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-fsx-filesystem-return-values"></a>

### Ref<a name="aws-resource-fsx-filesystem-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the function returns the file system resource ID\. For example:

`{"Ref":"fs-01234567890123456"}`

For the Amazon FSx file system `fs-01234567890123456`, Ref returns the file system ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-fsx-filesystem--examples"></a>

### Create an Amazon FSx for Lustre File System<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Lustre_File_System"></a>

The following examples create an Amazon FSx for Lustre file system\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Lustre_File_System--json"></a>

```
{
   "Resources": {
	  "BasicS3LinkedLustreFileSystem": {
		 "Type": "AWS::FSx::FileSystem",
		  "Properties": {
			 "FileSystemType": "LUSTRE",
			 "StorageCapacity": 3600,
			 "SubnetIds": [
				null
			],
			"SecurityGroupIds": [
				null
			],
			"Tags": [
			   {
				  "Key": "Name",
				  "Value": "s3linkedLustre"
			   },
			   {
				  "Key": "StorageCapacity",
				  "Value": "3600GB"
			   }
			],
			"LustreConfiguration": {
			   "ImportPath": null,
			   "ExportPath": null,
			   "WeeklyMaintenanceStartTime": "2:20:30"
			  }
	    }
	  }
	},
	"Outputs": {
	   "FileSystemId": {
		  "Value": null
		}
	}
}
```

#### YAML<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Lustre_File_System--yaml"></a>

```
Resources:
  BasicS3LinkedLustreFileSystem:
    Type: AWS::FSx::FileSystem
    Properties:
      FileSystemType: "LUSTRE"
      StorageCapacity: 3600
      SubnetIds: [!ImportValue CustomerPublicSubnet01]
      SecurityGroupIds: [!ImportValue LustreIngressSecurityGroupId]
      Tags:
        - Key: "Name"
          Value: "s3linkedLustre"
        - Key: "StorageCapacity"
          Value: "3600GB"
      LustreConfiguration:
        ImportPath: !Join ["", ["s3://", !ImportValue LustreCFNTestS3ImportBucketName]]
        ExportPath: !Join ["", ["s3://", !ImportValue LustreCFNTestS3ImportBucketName]]
        WeeklyMaintenanceStartTime: "2:20:30"
Outputs:
  FileSystemId:
    Value: !Ref BasicS3LinkedLustreFileSystemOutputs:
  FileSystemId:
Value: !Ref BasicS3LinkedLustreFileSystem
```

### Create an Amazon FSx for Windows File Server File System<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System"></a>

The following examples create an Amazon FSx for Windows File Server file system\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System--json"></a>

```
{
   "Resources": {
      "WindowsFileSystemWithAllConfigs": {
         "Type": "AWS::FSx::FileSystem",
         "Properties": {
            "FileSystemType": "WINDOWS",
            "StorageCapacity": 300,
            "SubnetIds": [
               null
            ],
            "SecurityGroupIds": [
               null
            ],
            "Tags": [
               {
                  "Key": "Name",
                  "Value": "windows"
               },
               {
                  "Key": "ThroughputCapacity",
                  "Value": "16"
               }
            ],
            "WindowsConfiguration": {
               "ActiveDirectoryId": null,
               "ThroughputCapacity": 8,
               "WeeklyMaintenanceStartTime": "4:16:30",
               "DailyAutomaticBackupStartTime": "01:00",
               "AutomaticBackupRetentionDays": 2,
               "CopyTagsToBackups": false
            }
         }
      }
   },
   "Outputs": {
      "FileSystemId": {
         "Value": null
      }
   }
}
```

#### YAML<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System--yaml"></a>

```
Resources:
  WindowsFileSystemWithAllConfigs:
    Type: "AWS::FSx::FileSystem"
    Properties:
      FileSystemType: "WINDOWS"
      StorageCapacity: 300
      SubnetIds: [!ImportValue CustomerPublicSubnet01]
      SecurityGroupIds: [!ImportValue LustreIngressSecurityGroupId]
      Tags:
        - Key: "Name"
          Value: "windows"
        - Key: "ThroughputCapacity"
          Value: "16"
      WindowsConfiguration:
        ActiveDirectoryId: !ImportValue CustomerDirectoryServiceId
        ThroughputCapacity: 8
        WeeklyMaintenanceStartTime: "4:16:30"
        DailyAutomaticBackupStartTime: "01:00"
        AutomaticBackupRetentionDays: 2
        CopyTagsToBackups: false
Outputs:
  FileSystemId:
Value: !Ref WindowsFileSystemWithAllConfigs
```
