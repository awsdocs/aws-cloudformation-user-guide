# AWS::FSx::DataRepositoryAssociation<a name="aws-resource-fsx-datarepositoryassociation"></a>

Creates an Amazon FSx for Lustre data repository association \(DRA\)\. A data repository association is a link between a directory on the file system and an Amazon S3 bucket or prefix\. You can have a maximum of 8 data repository associations on a file system\. Data repository associations are supported only for file systems with the `Persistent_2` deployment type\.

Each data repository association must have a unique Amazon FSx file system directory and a unique S3 bucket or prefix associated with it\. You can configure a data repository association for automatic import only, for automatic export only, or for both\. To learn more about linking a data repository to your file system, see [Linking your file system to an S3 bucket](https://docs.aws.amazon.com/fsx/latest/LustreGuide/create-dra-linked-data-repo.html)\.

## Syntax<a name="aws-resource-fsx-datarepositoryassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fsx-datarepositoryassociation-syntax.json"></a>

```
{
  "Type" : "AWS::FSx::DataRepositoryAssociation",
  "Properties" : {
      "[BatchImportMetaDataOnCreate](#cfn-fsx-datarepositoryassociation-batchimportmetadataoncreate)" : Boolean,
      "[DataRepositoryPath](#cfn-fsx-datarepositoryassociation-datarepositorypath)" : String,
      "[FileSystemId](#cfn-fsx-datarepositoryassociation-filesystemid)" : String,
      "[FileSystemPath](#cfn-fsx-datarepositoryassociation-filesystempath)" : String,
      "[ImportedFileChunkSize](#cfn-fsx-datarepositoryassociation-importedfilechunksize)" : Integer,
      "[S3](#cfn-fsx-datarepositoryassociation-s3)" : S3,
      "[Tags](#cfn-fsx-datarepositoryassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-fsx-datarepositoryassociation-syntax.yaml"></a>

```
Type: AWS::FSx::DataRepositoryAssociation
Properties: 
  [BatchImportMetaDataOnCreate](#cfn-fsx-datarepositoryassociation-batchimportmetadataoncreate): Boolean
  [DataRepositoryPath](#cfn-fsx-datarepositoryassociation-datarepositorypath): String
  [FileSystemId](#cfn-fsx-datarepositoryassociation-filesystemid): String
  [FileSystemPath](#cfn-fsx-datarepositoryassociation-filesystempath): String
  [ImportedFileChunkSize](#cfn-fsx-datarepositoryassociation-importedfilechunksize): Integer
  [S3](#cfn-fsx-datarepositoryassociation-s3): 
    S3
  [Tags](#cfn-fsx-datarepositoryassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-fsx-datarepositoryassociation-properties"></a>

`BatchImportMetaDataOnCreate`  <a name="cfn-fsx-datarepositoryassociation-batchimportmetadataoncreate"></a>
A boolean flag indicating whether an import data repository task to import metadata should run after the data repository association is created\. The task runs if this flag is set to `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataRepositoryPath`  <a name="cfn-fsx-datarepositoryassociation-datarepositorypath"></a>
The path to the Amazon S3 data repository that will be linked to the file system\. The path can be an S3 bucket or prefix in the format `s3://myBucket/myPrefix/`\. This path specifies where in the S3 data repository files will be imported from or exported to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `4357`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{3,4357}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemId`  <a name="cfn-fsx-datarepositoryassociation-filesystemid"></a>
The ID of the file system on which the data repository association is configured\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemPath`  <a name="cfn-fsx-datarepositoryassociation-filesystempath"></a>
A path on the Amazon FSx for Lustre file system that points to a high\-level directory \(such as `/ns1/`\) or subdirectory \(such as `/ns1/subdir/`\) that will be mapped 1\-1 with `DataRepositoryPath`\. The leading forward slash in the name is required\. Two data repository associations cannot have overlapping file system paths\. For example, if a data repository is associated with file system path `/ns1/`, then you cannot link another data repository with file system path `/ns1/ns2`\.  
This path specifies where in your file system files will be exported from or imported to\. This file system directory can be linked to only one Amazon S3 bucket, and no other S3 bucket can be linked to the directory\.  
If you specify only a forward slash \(`/`\) as the file system path, you can link only one data repository to the file system\. You can only specify "/" as the file system path for the first data repository associated with a file system\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,4096}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImportedFileChunkSize`  <a name="cfn-fsx-datarepositoryassociation-importedfilechunksize"></a>
For files imported from a data repository, this value determines the stripe count and maximum amount of data per file \(in MiB\) stored on a single physical disk\. The maximum number of disks that a single file can be striped across is limited by the total number of disks that make up the file system or cache\.  
The default chunk size is 1,024 MiB \(1 GiB\) and can go as high as 512,000 MiB \(500 GiB\)\. Amazon S3 objects have a maximum size of 5 TB\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `512000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-fsx-datarepositoryassociation-s3"></a>
The configuration for an Amazon S3 data repository linked to an Amazon FSx Lustre file system with a data repository association\. The configuration defines which file events \(new, changed, or deleted files or directories\) are automatically imported from the linked data repository to the file system or automatically exported from the file system to the data repository\.  
*Required*: No  
*Type*: [S3](aws-properties-fsx-datarepositoryassociation-s3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-fsx-datarepositoryassociation-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-fsx-datarepositoryassociation-return-values"></a>

### Ref<a name="aws-resource-fsx-datarepositoryassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the data repository association resource ID\. For example:

`{"Ref":"data_repository_association_logical_id"}`

Returns `dra-0123456789abcdef6`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fsx-datarepositoryassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-fsx-datarepositoryassociation-return-values-fn--getatt-fn--getatt"></a>

`AssociationId`  <a name="AssociationId-fn::getatt"></a>
Returns the data repository association's system generated Association ID\.  
Example: `dra-abcdef0123456789d`

`ResourceARN`  <a name="ResourceARN-fn::getatt"></a>
Returns the data repository association's Amazon Resource Name \(ARN\)\.  
Example: `arn:aws:fsx:us-east-1:111122223333:association/fs-abc012345def6789a/dra-abcdef0123456789b`

## Examples<a name="aws-resource-fsx-datarepositoryassociation--examples"></a>

### Create an Amazon FSx for Lustre data repository association<a name="aws-resource-fsx-datarepositoryassociation--examples--Create_an_Amazon_FSx_for_Lustre_data_repository_association"></a>

The following examples create a data repository association \(DRA\) that links an Amazon FSx for Lustre file system \(with the `Persistent_2` deployment type\) to an Amazon S3 bucket\.

#### JSON<a name="aws-resource-fsx-datarepositoryassociation--examples--Create_an_Amazon_FSx_for_Lustre_data_repository_association--json"></a>

```
{
    "Description": "FSx DRA with all properties.",
    "Parameters": {
        "FSId": {
            "Type": "String"
        },
        "DRAIdExportName": {
            "Type": "String"
        },
        "FileSystemPath": {
            "Type": "String"
        },
        "ImportedFileChunkSize": {
            "Type": "String"
        }
    },
    "Resources": {
        "TestDRA": {
            "Type": "AWS::FSx::DataRepositoryAssociation",
            "Properties": {
                "FileSystemId": {
                    "Ref": "FSId"
                },
                "FileSystemPath": {
                    "Ref": "FileSystemPath"
                },
                "DataRepositoryPath": "s3://example-bucket",
                "BatchImportMetaDataOnCreate": true,
                "ImportedFileChunkSize": {
                    "Ref": "ImportedFileChunkSize"
                },
                "S3": {
                    "AutoImportPolicy": {
                        "Events": [
                            "NEW",
                            "CHANGED",
                            "DELETED"
                        ]
                    },
                    "AutoExportPolicy": {
                        "Events": [
                            "NEW",
                            "CHANGED",
                            "DELETED"
                        ]
                    }
                },
                "Tags": [
                    {
                        "Key": "Location",
                        "Value": "Boston"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "DRAId": {
            "Value": {
                "Ref": "TestDRA"
            },
            "Export": {
                "Name": {
                    "Ref": "DRAIdExportName"
                }
            }
        }
    }
```

#### YAML<a name="aws-resource-fsx-datarepositoryassociation--examples--Create_an_Amazon_FSx_for_Lustre_data_repository_association--yaml"></a>

```
Description: "FSx DRA with all properties."
Parameters:
  FSId:
    Type: String
  DRAIdExportName:
    Type: String
  FileSystemPath:
    Type: String
  ImportedFileChunkSize:
    Type: String
Resources:
  TestDRA:
    Type: 'AWS::FSx::DataRepositoryAssociation'
    Properties:
      FileSystemId: !Ref FSId
      FileSystemPath: !Ref FileSystemPath
      DataRepositoryPath: "s3://example-bucket"
      BatchImportMetaDataOnCreate: true
      ImportedFileChunkSize: !Ref ImportedFileChunkSize
      S3:
        AutoImportPolicy:
          Events:
            - NEW
            - CHANGED
            - DELETED
        AutoExportPolicy:
          Events:
            - NEW
            - CHANGED
            - DELETED
      Tags:
        - Key: Location
          Value: Boston
Outputs:
  DRAId:
    Value: !Ref TestDRA
    Export:
      Name: !Ref DRAIdExportName
```