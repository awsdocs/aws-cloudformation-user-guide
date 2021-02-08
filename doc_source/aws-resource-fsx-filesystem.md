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
      "[LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration)" : LustreConfiguration,
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
  [KmsKeyId](#cfn-fsx-filesystem-kmskeyid): String
  [LustreConfiguration](#cfn-fsx-filesystem-lustreconfiguration): 
    LustreConfiguration
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
The ID of the backup\. Specifies the backup to use if you're creating a file system from an existing backup\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemType`  <a name="cfn-fsx-filesystem-filesystemtype"></a>
The type of Amazon FSx file system, either `LUSTRE` or `WINDOWS`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `LUSTRE | WINDOWS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KmsKeyId`  <a name="cfn-fsx-filesystem-kmskeyid"></a>
The ID of the AWS Key Management Service \(AWS KMS\) key used to encrypt the file system's data for Amazon FSx for Windows File Server file systems and persistent Amazon FSx for Lustre file systems at rest\. In either case, if not specified, the Amazon FSx managed key is used\. The scratch Amazon FSx for Lustre file systems are always encrypted at rest using Amazon FSx managed keys\. For more information, see [Encrypt](https://docs.aws.amazon.com/kms/latest/APIReference/API_Encrypt.html) in the *AWS Key Management Service API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LustreConfiguration`  <a name="cfn-fsx-filesystem-lustreconfiguration"></a>
The Lustre configuration for the file system being created\.   
*Required*: No  
*Type*: [LustreConfiguration](aws-properties-fsx-filesystem-lustreconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-fsx-filesystem-securitygroupids"></a>
A list of IDs specifying the security groups to apply to all network interfaces created for file system access\. This list isn't returned in later requests to describe the file system\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageCapacity`  <a name="cfn-fsx-filesystem-storagecapacity"></a>
Sets the storage capacity of the file system that you're creating\. `StorageCapacity` is required if you are creating a new file system\. Do not include `StorageCapacity` if you are creating a file system from a backup\.  
For Lustre file systems:  
+ For `SCRATCH_2` and `PERSISTENT_1 SSD` deployment types, valid values are 1200 GiB, 2400 GiB, and increments of 2400 GiB\.
+ For `PERSISTENT HDD` file systems, valid values are increments of 6000 GiB for 12 MB/s/TiB file systems and increments of 1800 GiB for 40 MB/s/TiB file systems\.
+ For `SCRATCH_1` deployment type, valid values are 1200 GiB, 2400 GiB, and increments of 3600 GiB\.
For Windows file systems:  
+ If `StorageType=SSD`, valid values are 32 GiB \- 65,536 GiB \(64 TiB\)\.
+ If `StorageType=HDD`, valid values are 2000 GiB \- 65,536 GiB \(64 TiB\)\.
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageType`  <a name="cfn-fsx-filesystem-storagetype"></a>
Sets the storage type for the file system you're creating\. Valid values are `SSD` and `HDD`\.  
+ Set to `SSD` to use solid state drive storage\. SSD is supported on all Windows and Lustre deployment types\.
+ Set to `HDD` to use hard disk drive storage\. HDD is supported on `SINGLE_AZ_2` and `MULTI_AZ_1` Windows file system deployment types, and on `PERSISTENT` Lustre file system deployment types\. 
 Default value is `SSD`\. For more information, see [ Storage Type Options](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/optimize-fsx-costs.html#storage-type-options) in the *Amazon FSx for Windows User Guide* and [Multiple Storage Options](https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html#storage-options) in the *Amazon FSx for Lustre User Guide*\.   
*Required*: No  
*Type*: String  
*Allowed values*: `HDD | SSD`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-fsx-filesystem-subnetids"></a>
Specifies the IDs of the subnets that the file system will be accessible from\. For Windows `MULTI_AZ_1` file system deployment types, provide exactly two subnet IDs, one for the preferred file server and one for the standby file server\. You specify one of these subnets as the preferred subnet using the `WindowsConfiguration > PreferredSubnetID` property\.  
For Windows `SINGLE_AZ_1` and `SINGLE_AZ_2` file system deployment types and Lustre file systems, provide exactly one subnet ID\. The file server is launched in that subnet's Availability Zone\.  
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

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the function returns the file system resource ID\. For example:

`{"Ref":"fs-01234567890123456"}`

For the Amazon FSx file system `fs-01234567890123456`, Ref returns the file system ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fsx-filesystem-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-fsx-filesystem-return-values-fn--getatt-fn--getatt"></a>

`LustreMountName`  <a name="LustreMountName-fn::getatt"></a>
Use the LustreMountName value when mounting an Amazon FSx for Lustre file system\. For SCRATCH\_1 deployment types, this value is always "fsx"\. For SCRATCH\_2 and PERSISTENT\_1 deployment types, this value is a string that is unique within an AWS Region\. For more information, see [Mounting from an Amazon EC2 Instance](https://docs.aws.amazon.com/fsx/latest/LustreGuide/mounting-ec2-instance.html)\.

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
        ImportPath: !Join ["", ["s3://", !ImportValue LustreCFNS3ImportBucketName]]
        ExportPath: !Join ["", ["s3://", !ImportValue LustreCFNS3ExportPath]]
        WeeklyMaintenanceStartTime: "2:20:30"
Outputs:
  FileSystemId:
    Value: !Ref BasicS3LinkedLustreFileSystem
```

### Create an Amazon FSx for Windows File Server File System in a Self\-managed Active Directory<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_a_Self-managed_Active_Directory"></a>

The following examples create a Multi\-AZ Amazon FSx for Windows File Server file system joined to a Self\-managed active directory\.

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
                    "WeeklyMaintenanceStartTime": "4:16:30",
                    "DailyAutomaticBackupStartTime": "01:00",
                    "AutomaticBackupRetentionDays": 30,
                    "CopyTagsToBackups": false,
                    "DeploymentType": "MULTI_AZ_1",
                    "PreferredSubnetId": {
                        "Fn:ImportValue": "MySubnet01"
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

### Create an Amazon FSx for Windows File Server File System in an AWS Managed Active Directory<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_an_AWS_Managed_Active_Directory"></a>

The following examples create a Multi\-AZ Amazon FSx for Windows File Server file system using HDD storage that is joined to an AWS Managed Active Directory\.

#### JSON<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_an_AWS_Managed_Active_Directory--json"></a>

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
                    "WeeklyMaintenanceStartTime": "4:16:30",
                    "DailyAutomaticBackupStartTime": "01:00",
                    "AutomaticBackupRetentionDays": 90,
                    "CopyTagsToBackups": false,
                    "DeploymentType": "MULTI_AZ_1",
                    "PreferredSubnetId": {
                        "Fn:ImportValue": "CfnFsxMadSubnet01"
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

#### YAML<a name="aws-resource-fsx-filesystem--examples--Create_an_Amazon_FSx_for_Windows_File_Server_File_System_in_an_AWS_Managed_Active_Directory--yaml"></a>

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