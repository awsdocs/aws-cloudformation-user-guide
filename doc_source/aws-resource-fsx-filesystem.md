# AWS::FSx::FileSystem<a name="aws-resource-fsx-filesystem"></a>

The `AWS::FSx::FileSystem` resource creates a new Amazon FSx file system\. You must specify the type Amazon FSx file system to create, Microsoft Windows \([WindowsConfiguration](#cfn-fsx-filesystem-windowsconfiguration)\) or Lustre \([LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration)\)\. For more information, see [CreateFileSystem](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateFileSystem.html) in the *Amazon FSx API Reference*\. 

## Syntax<a name="aws-resource-fsx-filesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax\.

### JSON<a name="aws-resource-fsx-filesystem-syntax.json"></a>

```
{
  "Type" : "AWS::FSx::FileSystem",
  "Properties" : {
    "[BackupId](#cfn-fsx-filesystem-backupid)" : String,
    "[FileSystemType](#cfn-fsx-filesystem-filesystemtype)" : String,
    "[KmsKeyId](#cfn-fsx-filesystem-kmskeyid)" : String,
    "[LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration)" : [*LustreConfiguration*](aws-properties-fsx-filesystem-lustreconfiguration.md),
    "[SecurityGroupIds](#cfn-fsx-filesystem-securitygroupids)" : [ String, ... ],
    "[StorageCapacity](#cfn-fsx-filesystem-storagecapacity)" : Integer,
    "[SubnetIds](#cfn-fsx-filesystem-subnetids)" : [ String, ... ],
    "[Tags](#cfn-fsx-filesystem-tags)" : [ [*Resource Tag*](aws-properties-resource-tags.md), ... ],
    "[WindowsConfiguration](#cfn-fsx-filesystem-windowsconfiguration)" : [*WindowsConfiguration*](aws-properties-fsx-filesystem-windowsconfiguration.md)
  }
}
```

### YAML<a name="aws-resource-fsx-filesystem-syntax.yaml"></a>

```
Type: "AWS::FSx::FileSystem"
Properties:
  [BackupId](#cfn-fsx-filesystem-backupid): String
  [FileSystemType](#cfn-fsx-filesystem-filesystemtype): String
  [KmsKeyId](#cfn-fsx-filesystem-kmskeyid): String
  [LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration): 
    [*LustreConfiguration*](aws-properties-fsx-filesystem-lustreconfiguration.md)
  [SecurityGroupIds](#cfn-fsx-filesystem-securitygroupids): 
    - String
  [StorageCapacity](#cfn-fsx-filesystem-storagecapacity): Integer
  [SubnetIds](#cfn-fsx-filesystem-subnetids): 
    - String
  [Tags](#cfn-fsx-filesystem-tags): 
    - [*Resource Tag*](aws-properties-resource-tags.md)
  [WindowsConfiguration](#cfn-fsx-filesystem-windowsconfiguration): 
    [*WindowsConfiguration*](aws-properties-fsx-filesystem-windowsconfiguration.md)
```

## Properties<a name="aws-resource-fsx-filesystem-properties"></a>

`BackupId`  <a name="cfn-fsx-filesystem-backupid"></a>
The ID of the backup of an Amazon FSx for Windows File Server file system\. For more information, see [CreateBackup](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateBackup.html) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`FileSystemType`  <a name="cfn-fsx-filesystem-filesystemtype"></a>
The type of file system\. For more information, see [FileSystem](https://docs.aws.amazon.com/fsx/latest/APIReference/API_FileSystem.html) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`KmsKeyId`  <a name="cfn-fsx-filesystem-kmskeyid"></a>
The ID of the AWS Key Management Service \(AWS KMS\) key used to encrypt the file system's data for an Amazon FSx for Windows File Server file system\. For more information, see [CreateFileSystem](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateFileSystem.html) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LustreConfiguration`  <a name="cfn-fsx-filesystem-lustreconfiguration"></a>
The configuration for the Amazon FSx for Lustre file system\. For more information, see [LustreFileSystemConfiguration](https://docs.aws.amazon.com/fsx/latest/APIReference/API_LustreFileSystemConfiguration.html) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: [LustreConfiguration](aws-properties-fsx-filesystem-lustreconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SecurityGroupIds`  <a name="cfn-fsx-filesystem-securitygroupids"></a>
A list of IDs for the security groups that apply to the specified network interfaces created for file system access\. These security groups apply to all network interfaces\. This list isn't returned in later describe requests\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`StorageCapacity`  <a name="cfn-fsx-filesystem-storagecapacity"></a>
The storage capacity of the file system\. For Windows file systems, the storage capacity has a minimum of 300 GiB, and a maximum of 65,536 GiB\. For Lustre file systems, the storage capacity has a minimum of 3,600 GiB, and is provisioned in increments of 3,600 GiB\. For more information, see [StorageCapacity](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateFileSystem.html#FSx-CreateFileSystem-request-StorageCapacity) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SubnetIds`  <a name="cfn-fsx-filesystem-subnetids"></a>
A list of IDs for the subnets that the file system will be accessible from\. File systems support only one subnet\. The file server is also launched in that subnet's Availability Zone\. For more information, see [SubnetIds](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateFileSystem.html#FSx-CreateFileSystem-request-SubnetIds) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-fsx-filesystem-tags"></a>
The tags to be applied to the file system at file system creation\. The key value of the `Name` tag appears in the console as the file system name\. For more information, see [Tags](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateFileSystem.html#FSx-CreateFileSystem-request-Tags) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`WindowsConfiguration`  <a name="cfn-fsx-filesystem-windowsconfiguration"></a>
The configuration for a Microsoft Windows file system\. For more information, see [WindowsFileSystemConfiguration](https://docs.aws.amazon.com/fsx/latest/APIReference/API_WindowsFileSystemConfiguration.html) in the *Amazon FSx API Reference*\.  
 *Required*: No  
 *Type*: [WindowsConfiguration](aws-properties-fsx-filesystem-windowsconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-fsx-filesystem-returnvalues"></a>

### Ref<a name="aws-resource-fsx-filesystem-ref"></a>

When you pass the logical ID of an `AWS::FSx::FileSystem` resource to the intrinsic `Ref` function, the function returns the file system resource ID, such as `fs-0d33333e999a7c66g`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-fsx-filesystem-examples"></a>

### Create an Amazon FSx for Lustre File System<a name="aws-resource-fsx-filesystem-example1"></a>

The following examples create an Amazon FSx for Lustre file system\.

#### JSON<a name="aws-resource-fsx-filesystem-example1.json"></a>

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

#### YAML<a name="aws-resource-fsx-filesystem-example1.yaml"></a>

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

### Create an Amazon FSx for Windows File Server File System<a name="aws-resource-fsx-filesystem-example2"></a>

The following examples create an Amazon FSx for Windows File Server file system\.

#### JSON<a name="aws-resource-fsx-filesystem-example2.json"></a>

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

#### YAML<a name="aws-resource-fsx-filesystem-example2.yaml"></a>

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