# AWS::FSx::FileSystem<a name="aws-resource-fsx-filesystem"></a>

The `AWS::FSx::FileSystem` resource is an Amazon FSx resource type that specifies an Amazon FSx file system\. You can create any of the following supported file system types:
+ Amazon FSx for Lustre
+ Amazon FSx for NetApp ONTAP
+ Amazon FSx for OpenZFS
+ Amazon FSx for Windows File Server

## Syntax<a name="aws-resource-fsx-filesystem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fsx-filesystem-syntax.json"></a>

```
{
  "Type" : "AWS::FSx::FileSystem",
  "Properties" : {
      "[BackupId](#cfn-fsx-filesystem-backupid)" : String,
      "[FileSystemType](#cfn-fsx-filesystem-filesystemtype)" : String,
      "[FileSystemTypeVersion](#cfn-fsx-filesystem-filesystemtypeversion)" : String,
      "[KmsKeyId](#cfn-fsx-filesystem-kmskeyid)" : String,
      "[LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration)" : LustreConfiguration,
      "[OntapConfiguration](#cfn-fsx-filesystem-ontapconfiguration)" : OntapConfiguration,
      "[OpenZFSConfiguration](#cfn-fsx-filesystem-openzfsconfiguration)" : OpenZFSConfiguration,
      "[SecurityGroupIds](#cfn-fsx-filesystem-securitygroupids)" : [ String, ... ],
      "[StorageCapacity](#cfn-fsx-filesystem-storagecapacity)" : Integer,
      "[StorageType](#cfn-fsx-filesystem-storagetype)" : String,
      "[SubnetIds](#cfn-fsx-filesystem-subnetids)" : [ String, ... ],
      "[Tags](#cfn-fsx-filesystem-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WindowsConfiguration](#cfn-fsx-filesystem-windowsconfiguration)" : WindowsConfiguration
    }
}
```

### YAML<a name="aws-resource-fsx-filesystem-syntax.yaml"></a>

```
Type: AWS::FSx::FileSystem
Properties: 
  [BackupId](#cfn-fsx-filesystem-backupid): String
  [FileSystemType](#cfn-fsx-filesystem-filesystemtype): String
  [FileSystemTypeVersion](#cfn-fsx-filesystem-filesystemtypeversion): String
  [KmsKeyId](#cfn-fsx-filesystem-kmskeyid): String
  [LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration): 
    LustreConfiguration
  [OntapConfiguration](#cfn-fsx-filesystem-ontapconfiguration): 
    OntapConfiguration
  [OpenZFSConfiguration](#cfn-fsx-filesystem-openzfsconfiguration): 
    OpenZFSConfiguration
  [SecurityGroupIds](#cfn-fsx-filesystem-securitygroupids): 
    - String
  [StorageCapacity](#cfn-fsx-filesystem-storagecapacity): Integer
  [StorageType](#cfn-fsx-filesystem-storagetype): String
  [SubnetIds](#cfn-fsx-filesystem-subnetids): 
    - String
  [Tags](#cfn-fsx-filesystem-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WindowsConfiguration](#cfn-fsx-filesystem-windowsconfiguration): 
    WindowsConfiguration
```

## Properties<a name="aws-resource-fsx-filesystem-properties"></a>

`BackupId`  <a name="cfn-fsx-filesystem-backupid"></a>
The ID of the file system backup that you are using to create a file system\. For more information, see [CreateFileSystemFromBackup](https://docs.aws.amazon.com/fsx/latest/APIReference/API_CreateFileSystemFromBackup.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemType`  <a name="cfn-fsx-filesystem-filesystemtype"></a>
The type of Amazon FSx file system, which can be `LUSTRE`, `WINDOWS`, `ONTAP`, or `OPENZFS`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemTypeVersion`  <a name="cfn-fsx-filesystem-filesystemtypeversion"></a>
\(Optional\) For FSx for Lustre file systems, sets the Lustre version for the file system that you're creating\. Valid values are `2.10` and `2.12`:  
+ 2\.10 is supported by the Scratch and Persistent\_1 Lustre deployment types\.
+ 2\.12 is supported by all Lustre deployment types\. `2.12` is required when setting FSx for Lustre `DeploymentType` to `PERSISTENT_2`\.
Default value = `2.10`, except when `DeploymentType` is set to `PERSISTENT_2`, then the default is `2.12`\.  
If you set `FileSystemTypeVersion` to `2.10` for a `PERSISTENT_2` Lustre deployment type, the `CreateFileSystem` operation fails\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `20`  
*Pattern*: `^[0-9](.[0-9]*)*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-fsx-filesystem-kmskeyid"></a>
The ID of the AWS Key Management Service \(AWS KMS\) key used to encrypt Amazon FSx file system data\. Used as follows with Amazon FSx file system types:  
+ Amazon FSx for Lustre `PERSISTENT_1` and `PERSISTENT_2` deployment types only\.

   `SCRATCH_1` and `SCRATCH_2` types are encrypted using the Amazon FSx service AWS KMS key for your account\.
+ Amazon FSx for NetApp ONTAP
+ Amazon FSx for OpenZFS
+ Amazon FSx for Windows File Server
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LustreConfiguration`  <a name="cfn-fsx-filesystem-lustreconfiguration"></a>
The Lustre configuration for the file system being created\.  
The following parameters are not supported for file systems with the Lustre `Persistent_2` deployment type\.  
+  `AutoImportPolicy` 
+  `ExportPath` 
+  `ImportedChunkSize` 
+  `ImportPath` 
*Required*: Conditional  
*Type*: [LustreConfiguration](aws-properties-fsx-filesystem-lustreconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OntapConfiguration`  <a name="cfn-fsx-filesystem-ontapconfiguration"></a>
The ONTAP configuration properties of the FSx for ONTAP file system that you are creating\.  
*Required*: No  
*Type*: [OntapConfiguration](aws-properties-fsx-filesystem-ontapconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenZFSConfiguration`  <a name="cfn-fsx-filesystem-openzfsconfiguration"></a>
The Amazon FSx for OpenZFS configuration properties for the file system that you are creating\.  
*Required*: No  
*Type*: [OpenZFSConfiguration](aws-properties-fsx-filesystem-openzfsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-fsx-filesystem-securitygroupids"></a>
A list of IDs specifying the security groups to apply to all network interfaces created for file system access\. This list isn't returned in later requests to describe the file system\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageCapacity`  <a name="cfn-fsx-filesystem-storagecapacity"></a>
Sets the storage capacity of the file system that you're creating\. `StorageCapacity` is required if you are creating a new file system\.  
**FSx for Lustre file systems** \- The amount of storage capacity that you can configure depends on the value that you set for `StorageType` and the Lustre `DeploymentType`, as follows:  
+ For `SCRATCH_2`, `PERSISTENT_2` and `PERSISTENT_1` deployment types using SSD storage type, the valid values are 1200 GiB, 2400 GiB, and increments of 2400 GiB\.
+ For `PERSISTENT_1` HDD file systems, valid values are increments of 6000 GiB for 12 MB/s/TiB file systems and increments of 1800 GiB for 40 MB/s/TiB file systems\.
+ For `SCRATCH_1` deployment type, valid values are 1200 GiB, 2400 GiB, and increments of 3600 GiB\.
**FSx for ONTAP file systems** \- The amount of storage capacity that you can configure is from 1024 GiB up to 196,608 GiB \(192 TiB\)\.  
**FSx for OpenZFS file systems** \- The amount of storage capacity that you can configure is from 64 GiB up to 524,288 GiB \(512 TiB\)\. If you are creating a file system from a backup, you can specify a storage capacity equal to or greater than the original file system's storage capacity\.  
**FSx for Windows File Server file systems** \- The amount of storage capacity that you can configure depends on the value that you set for `StorageType` as follows:  
+ For SSD storage, valid values are 32 GiB\-65,536 GiB \(64 TiB\)\.
+ For HDD storage, valid values are 2000 GiB\-65,536 GiB \(64 TiB\)\.
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageType`  <a name="cfn-fsx-filesystem-storagetype"></a>
Sets the storage type for the file system that you're creating\. Valid values are `SSD` and `HDD`\.  
+ Set to `SSD` to use solid state drive storage\. SSD is supported on all Windows, Lustre, ONTAP, and OpenZFS deployment types\.
+ Set to `HDD` to use hard disk drive storage\. HDD is supported on `SINGLE_AZ_2` and `MULTI_AZ_1` Windows file system deployment types, and on `PERSISTENT_1` Lustre file system deployment types\. 
Default value is `SSD`\. For more information, see [ Storage type options](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/optimize-fsx-costs.html#storage-type-options) in the *FSx for Windows File Server User Guide* and [Multiple storage options](https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html#storage-options) in the *FSx for Lustre User Guide*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `HDD | SSD`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-fsx-filesystem-subnetids"></a>
Specifies the IDs of the subnets that the file system will be accessible from\. For Windows and ONTAP `MULTI_AZ_1` deployment types,provide exactly two subnet IDs, one for the preferred file server and one for the standby file server\. You specify one of these subnets as the preferred subnet using the `WindowsConfiguration > PreferredSubnetID` or `OntapConfiguration > PreferredSubnetID` properties\. For more information about Multi\-AZ file system configuration, see [ Availability and durability: Single\-AZ and Multi\-AZ file systems](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html) in the *Amazon FSx for Windows User Guide* and [ Availability and durability](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/high-availability-multiAZ.html) in the *Amazon FSx for ONTAP User Guide*\.  
For Windows `SINGLE_AZ_1` and `SINGLE_AZ_2` and all Lustre deployment types, provide exactly one subnet ID\. The file server is launched in that subnet's Availability Zone\.  
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
The configuration object for the Microsoft Windows file system you are creating\. This value is required if `FileSystemType` is set to `WINDOWS`\.  
*Required*: Conditional  
*Type*: [WindowsConfiguration](aws-properties-fsx-filesystem-windowsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-fsx-filesystem-return-values"></a>

### Ref<a name="aws-resource-fsx-filesystem-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the file system resource ID\. For example:

`{"Ref":"file_system_logical_id"}`

Returns `fs-0123456789abcdef6`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fsx-filesystem-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-fsx-filesystem-return-values-fn--getatt-fn--getatt"></a>

`DNSName`  <a name="DNSName-fn::getatt"></a>
Returns the FSx for Windows file system's DNSName\.  
Example: `amznfsxp1honlek.corp.example.com`

`LustreMountName`  <a name="LustreMountName-fn::getatt"></a>
Returns the Lustre file system's `LustreMountName`\.  
Example for `SCRATCH_1` deployment types: This value is always `fsx`\.  
Example for `SCRATCH_2` and `PERSISTENT` deployment types: `2p3fhbmv`

`ResourceARN`  <a name="ResourceARN-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the Amazon FSx file system\.  
Example: `arn:aws:fsx:us-east-2:111122223333:file-system/fs-0123abcd56789ef0a`

`RootVolumeId`  <a name="RootVolumeId-fn::getatt"></a>
Returns the root volume ID of the FSx for OpenZFS file system\.  
Example: `fsvol-0123456789abcdefa`

## Examples<a name="aws-resource-fsx-filesystem--examples"></a>



### Create an Amazon FSx for Lustre File System<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Lustre_File_System"></a>

The following examples create a 1\.2 TiB persistent Amazon FSx for Lustre file system, with a `PerUnitStorageThroughput` of 200 MB/s/TiB\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Lustre_File_System--json"></a>

```
{
    "Resources": {
        "BasicS3LinkedLustreFileSystem": {
            "Type": "AWS::FSx::FileSystem",
            "Properties": {
                "FileSystemType": "LUSTRE",
                "FileSystemTypeVersion": "2.12",
                "StorageCapacity": 1200,
                "SubnetIds": [
                    {
                        "Fn::ImportValue": "MySubnet01"
                    }
                ],
                "SecurityGroupIds": [
                    {
                        "Fn::ImportValue": "LustreIngressSecurityGroupId"
                    }
                ],
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "CFNs3linkedLustre"
                    }
                ],
                "LustreConfiguration": {
                    "AutoImportPolicy" : "NEW",               
                    "CopyTagsToBackups" : true,
                    "DeploymentType": "PERSISTENT_1",
                    "PerUnitStorageThroughput": 200,                    
                    "DataCompressionType": "LZ4",
                    "ImportPath": {
                        "Fn::Join": [
                            "",
                            [
                                "s3://",
                                {
                                    "Fn::ImportValue": "LustreCFNS3ImportBucketName"
                                }
                            ]
                        ]
                    },
                    "ExportPath": {
                        "Fn::Join": [
                            "",
                            [
                                "s3://",
                                {
                                    "Fn::ImportValue": "LustreCFNS3ExportPath"
                                }
                            ]
                        ]
                    },
                    "WeeklyMaintenanceStartTime": "2:20:30"
                }
            }
        }
    },
    "Outputs": {
        "FileSystemId": {
            "Value": {
                "Ref": "BasicS3LinkedLustreFileSystem"
            }
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
      FileSystemTypeVersion: "2.12"
      StorageCapacity: 1200
      SubnetIds: [!ImportValue MySubnet01]
      SecurityGroupIds: [!ImportValue LustreIngressSecurityGroupId]
      Tags:
        - Key: "Name"
          Value: "CFNs3linkedLustre"
      LustreConfiguration:
        AutoImportPolicy: "NEW"
        CopyTagsToBackups: true
        DeploymentType: "PERSISTENT_1"
        PerUnitStorageThroughput: 200
        DataCompressionType: "LZ4"
        ImportPath: !Join ["", ["s3://", !ImportValue LustreCFNS3ImportBucketName]]
        ExportPath: !Join ["", ["s3://", !ImportValue LustreCFNS3ExportPath]]
        WeeklyMaintenanceStartTime: "2:20:30"
Outputs:
  FileSystemId:
    Value: !Ref BasicS3LinkedLustreFileSystem
```

### Create an Amazon FSx for Windows File Server File System in a Self\-managed Active Directory<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_a_Self-managed_Active_Directory"></a>

The following examples create a Multi\-AZ Amazon FSx for Windows File Server file system joined to a self\-managed active directory\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_a_Self-managed_Active_Directory--json"></a>

```
{
    "Resources": {
        "WindowsSelfManagedADFileSystemWithAllConfigs": {
            "Type": "AWS::FSx::FileSystem",
            "Properties": {
                "FileSystemType": "WINDOWS",
                "StorageCapacity": 32,
                "StorageType": "SSD",
                "SubnetIds": [
                    {
                        "Fn::ImportValue": "MySubnet01"
                    },
                    {
                        "Fn::ImportValue": "MySubnet02"
                    }
                ],
                "SecurityGroupIds": [
                    {
                        "Fn::ImportValue": "WindowsIngressSecurityGroupId"
                    }
                ],
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "windows"
                    }
                ],
                "WindowsConfiguration": {
                    "ThroughputCapacity": 8,
                    "Aliases": [
                        "financials.corp.example.com"
                    ],
                    "WeeklyMaintenanceStartTime": "4:16:30",
                    "DailyAutomaticBackupStartTime": "01:00",
                    "AutomaticBackupRetentionDays": 30,
                    "CopyTagsToBackups": false,
                    "DeploymentType": "MULTI_AZ_1",
                    "PreferredSubnetId": {
                        "Fn::ImportValue": "MySubnet01"
                    },
                    "SelfManagedActiveDirectoryConfiguration": {
                        "DnsIps": [
                            {
                                "Fn::Select": [
                                    0,
                                    {
                                        "Fn::Split": [
                                            ",",
                                            {
                                                "Fn::ImportValue": "MySelfManagedADDnsIpAddresses"
                                            }
                                        ]
                                    }
                                ]
                            }
                        ],
                        "DomainName": {
                            "Fn::ImportValue": "SelfManagedADDomainName"
                        },
                        "FileSystemAdministratorsGroup": "MyDomainAdminGroup",
                        "OrganizationalUnitDistinguishedName": "OU=FileSystems,DC=corp,DC=example,DC=com",
                        "UserName": "Admin",
                        "Password": {
                            "Fn::Join": [
                                ":",
                                [
                                    "{{resolve:secretsmanager",
                                    {
                                        "Fn::ImportValue": "MySelfManagedADCredentialName"
                                    },
                                    "SecretString}}"
                                ]
                            ]
                        }
                    }
                }
            }
        }
    },
    "Outputs": {
        "FileSystemId": {
            "Value": {
                "Ref": "WindowsSelfManagedADFileSystemWithAllConfigs"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_a_Self-managed_Active_Directory--yaml"></a>

```
Resources:
  WindowsSelfManagedADFileSystemWithAllConfigs:
    Type: 'AWS::FSx::FileSystem'
    Properties:
      FileSystemType: WINDOWS
      StorageCapacity: 32
      StorageType: SSD
      SubnetIds:
        - !ImportValue MySubnet01
        - !ImportValue MySubnet02
      SecurityGroupIds:
        - !ImportValue WindowsIngressSecurityGroupId
      Tags:
        - Key: Name
          Value: windows
      WindowsConfiguration:
        ThroughputCapacity: 8
        Aliases: 
            - financials.corp.example.com         
        WeeklyMaintenanceStartTime: '4:16:30'
        DailyAutomaticBackupStartTime: '01:00'
        AutomaticBackupRetentionDays: 30
        CopyTagsToBackups: false
        DeploymentType: MULTI_AZ_1
        PreferredSubnetId: !ImportValue MySubnet01
        SelfManagedActiveDirectoryConfiguration:
          DnsIps:
            - !Select 
              - 0
              - !Split 
                - ','
                - !ImportValue MySelfManagedADDnsIpAddresses
          DomainName:
            'Fn::ImportValue': SelfManagedADDomainName
          FileSystemAdministratorsGroup: MyDomainAdminGroup
          OrganizationalUnitDistinguishedName: 'OU=FileSystems,DC=corp,DC=example,DC=com'
          UserName: Admin
          Password: !Join 
            - ':'
            - - '{{resolve:secretsmanager'
              - !ImportValue MySelfManagedADCredentialName
              - 'SecretString}}'
Outputs:
  FileSystemId:
    Value: !Ref WindowsSelfManagedADFileSystemWithAllConfigs
```

### Create an Amazon FSx for Windows File Server File System in an Amazon Managed Active Directory<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_an_Amazon_Managed_Active_Directory"></a>

The following examples create a Multi\-AZ Amazon FSx for Windows File Server file system using HDD storage that is joined to an AWS Managed Active Directory\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_an_Amazon_Managed_Active_Directory--json"></a>

```
{
    "Resources": {
        "WindowsMadFileSystemWithAllConfigs": {
            "Type": "AWS::FSx::FileSystem",
            "Properties": {
                "FileSystemType": "WINDOWS",
                "StorageCapacity": 2000,
                "StorageType": "HDD",
                "SubnetIds": [
                    {
                        "Fn::ImportValue": "CfnFsxMadSubnet01"
                    },
                    {
                        "Fn::ImportValue": "CfnFsxMadSubnet02"
                    }
                ],
                "SecurityGroupIds": [
                    {
                        "Fn::ImportValue": "WindowsIngressSecurityGroupId"
                    }
                ],
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "windows"
                    }
                ],
                "WindowsConfiguration": {
                    "ActiveDirectoryId": {
                        "Fn::ImportValue": "CfnFsxMadDirectoryServiceId"
                    },
                    "ThroughputCapacity": 8,
                    "Aliases": [
                        "financials.corp.example.com"
                    ],
                    "WeeklyMaintenanceStartTime": "4:16:30",
                    "DailyAutomaticBackupStartTime": "01:00",
                    "AutomaticBackupRetentionDays": 90,
                    "CopyTagsToBackups": false,
                    "DeploymentType": "MULTI_AZ_1",
                    "PreferredSubnetId": {
                        "Fn::ImportValue": "CfnFsxMadSubnet01"
                    }
                }
            }
        }
    },
    "Outputs": {
        "FileSystemId": {
            "Value": {
                "Ref": "WindowsMadFileSystemWithAllConfigs"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_an_Amazon_Managed_Active_Directory--yaml"></a>

```
Resources:
  WindowsMadFileSystemWithAllConfigs:
    Type: 'AWS::FSx::FileSystem'
    Properties:
      FileSystemType: WINDOWS
      StorageCapacity: 2000
      StorageType: SSD
      SubnetIds:
        - !ImportValue CfnFsxMadSubnet01
        - !ImportValue CfnFsxMadSubnet02
      SecurityGroupIds:
        - !ImportValue WindowsIngressSecurityGroupId
      Tags:
        - Key: Name
          Value: windows
      WindowsConfiguration:
        ActiveDirectoryId: !ImportValue CfnFsxMadDirectoryServiceId
        ThroughputCapacity: 8
        Aliases: 
            - financials.corp.example.com
        WeeklyMaintenanceStartTime: '4:16:30'
        DailyAutomaticBackupStartTime: '01:00'
        AutomaticBackupRetentionDays: 90
        DeploymentType: MULTI_AZ_1
        PreferredSubnetId: !ImportValue CfnFsxMadSubnet01
        CopyTagsToBackups: false
Outputs:
  FileSystemId:
    Value: !Ref WindowsMadFileSystemWithAllConfigs
```

### Create an Amazon FSx for Windows File Server File System with file access audit event logging enabled<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_with_file_access_audit_event_logging_enabled"></a>

The following examples create a Multi\-AZ Amazon FSx for Windows File Server file system with file access auditing enabled\. Audit event logs are emitted when end users make successful or failed attempts to access files, folders, and file shares on the file system\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_with_file_access_audit_event_logging_enabled--json"></a>

```
{
    "Resources": {
        "WindowsMadFileSystemWithAllConfigs": {
            "Type": "Dev::FSx::FileSystem",
            "Properties": {
                "FileSystemType": "WINDOWS",
                "StorageCapacity": 100,
                "SubnetIds": [
                    {
                        "Fn::ImportValue": "CfnFsxMadSubnet01"
                    },
                    {
                        "Fn::ImportValue": "CfnFsxMadSubnet02"
                    }
                ],
                "SecurityGroupIds": [
                    {
                        "Fn::ImportValue": "CfnWindowsIngressSecurityGroupId"
                    }
                ],
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "windows"
                    }
                ],
                "WindowsConfiguration": {
                    "ActiveDirectoryId": {
                        "Fn::ImportValue": "CfnFsxMadDirectoryServiceId"
                    },
                    "ThroughputCapacity": 32,
                    "DeploymentType": "MULTI_AZ_1",
                    "PreferredSubnetId": {
                        "Fn::ImportValue": "CfnFsxMadSubnet01"
                    }
                    "AuditLogConfiguration": {
                        "FileAccessAuditLogLevel": "SUCCESS_AND_FAILURE",
                        "FileShareAccessAuditLogLevel": "SUCCESS_AND_FAILURE",
                        "AuditLogDestination": 
                        {
                          "Fn::Select": [
                            0,
                            {
                              "Fn::Split": [
                                ":*",
                                {
                                  "Fn::ImportValue": "CfnWindowsFileAccessAuditingLogGroupArn"
                                }
                              ]
                            }
                          ]
                        }
                    }
                }
            }
        }
    },
    "Outputs": {
        "FileSystemId": {
             "Value": {
                "Ref": "WindowsMadFileSystemWithAllConfigs"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_with_file_access_audit_event_logging_enabled--yaml"></a>

```
Resources:
  WindowsMadFileSystemWithAllConfigs:
    Type: "AWS::FSx::FileSystem"
    Properties:
      FileSystemType: "WINDOWS"
      StorageCapacity: 100
      SubnetIds:
        - !ImportValue CfnFsxMadSubnet01
        - !ImportValue CfnFsxMadSubnet02
      SecurityGroupIds:
        - !ImportValue WindowsIngressSecurityGroupId
      Tags:
        - Key: Name
          Value: windows
      WindowsConfiguration:
        ActiveDirectoryId: !ImportValue CfnFsxMadDirectoryServiceId
        ThroughputCapacity: 32
        DeploymentType: MULTI_AZ_1
        PreferredSubnetId: !ImportValue CfnFsxMadSubnet01
        AuditLogConfiguration:
          FileAccessAuditLogLevel: "SUCCESS_AND_FAILURE"
          FileShareAccessAuditLogLevel: "SUCCESS_AND_FAILURE"
          AuditLogDestination: !Select
            - 0
            - !Split
              - ':*'
              - 'Fn::ImportValue': WindowsFileAccessAuditingLogGroupArn
                
Outputs:
    FileSystemId:
      Value: !Ref WindowsMadFileSystemWithAllConfigs
```

### Create an Amazon FSx for NetApp ONTAP File System<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_NetApp_ONTAP_File_System"></a>

The following examples create a 1 TiB Amazon FSx for NetApp ONTAP file system\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_NetApp_ONTAP_File_System--json"></a>

```
{
   "OntapMultiAzFileSystemWithAllConfigs": {
      "Type": "AWS::FSx::FileSystem",
      "Condition": "OntapMazEnabled",
      "Properties": {
         "FileSystemType": "ONTAP",
         "StorageCapacity": 1024,
         "StorageType": "SSD",
         "SubnetIds": [
         "subnet-1234567890abcdef0",
         "subnet-abcdef01234567890"
         ],
         "SecurityGroupIds": [
         "sg-021345abcdef6789"
         ],
         "OntapConfiguration": {
            "AutomaticBackupRetentionDays": 3,
            "DailyAutomaticBackupStartTime": "07:00",
            "DeploymentType": "MULTI_AZ_1",
            "DiskIopsConfiguration": {
               "Iops": 10000,
               "Mode": "USER_PROVISIONED"
            },
            "PreferredSubnetId": "subnet-abcdef01234567890",
            "RouteTableIds": [
            "rtb-abcdef01234567890"
            ],
            "ThroughputCapacity": 512,
            "WeeklyMaintenanceStartTime": "4:16:30"
         },
         "Tags": [
            {
               "Key": "Name",
               "Value": "OntapFileSystem_MAZ"
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_NetApp_ONTAP_File_System--yaml"></a>

```
OntapMultiAzFileSystemWithAllConfigs:
   Type: "AWS::FSx::FileSystem"
   Condition: OntapMazEnabled
   Properties:
      FileSystemType: "ONTAP"
      StorageCapacity: 1024
      StorageType: SSD
      SubnetIds: ["subnet-1234567890abcdef0", "subnet-abcdef01234567890"]
      SecurityGroupIds: ["sg-068ec2a396aa7c2c8"]
      OntapConfiguration:
         AutomaticBackupRetentionDays: 3
         DailyAutomaticBackupStartTime: "07:00"
         DeploymentType: "MULTI_AZ_1"
         DiskIopsConfiguration:
            Iops: 10000
            Mode: "USER_PROVISIONED"
         PreferredSubnetId: "subnet-abcdef01234567890"
         RouteTableIds: ["rtb-abcdef01234567890"]
         ThroughputCapacity: 512
         WeeklyMaintenanceStartTime: "4:16:30"
      Tags:
        - Key: "Name"
          Value: "OntapFileSystem_MAZ"
```