# AWS::SSM::ResourceDataSync<a name="aws-resource-ssm-resourcedatasync"></a>

The `AWS::SSM::ResourceDataSync` resource creates, updates, or deletes a Resource Data Sync for AWS Systems Manager\. A resource data sync helps you view data from multiple sources in a single location\. Systems Manager offers two types of resource data sync: `SyncToDestination` and `SyncFromSource`\.

You can configure Systems Manager Inventory to use the `SyncToDestination` type to synchronize Inventory data from multiple AWS Regions to a single Amazon S3 bucket\. 

You can configure Systems Manager Explorer to use the `SyncFromSource` type to synchronize operational work items \(OpsItems\) and operational data \(OpsData\) from multiple AWS Regions\. This type can synchronize OpsItems and OpsData from multiple AWS accounts and Regions or from an `EntireOrganization` by using AWS Organizations\.

A resource data sync is an asynchronous operation that returns immediately\. After a successful initial sync is completed, the system continuously syncs data\.

By default, data is not encrypted in Amazon S3\. We strongly recommend that you enable encryption in Amazon S3 to ensure secure data storage\. We also recommend that you secure access to the Amazon S3 bucket by creating a restrictive bucket policy\. 

For more information, see [Configuring Inventory Collection](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-inventory-configuring.html#sysman-inventory-datasync) and [Setting Up Systems Manager Explorer to Display Data from Multiple Accounts and Regions](https://docs.aws.amazon.com/systems-manager/latest/userguide/Explorer-resource-data-sync.html) in the *AWS Systems Manager User Guide*\.

Important: The following *Syntax* section shows all fields that are supported for a resource data sync\. The *Examples* section below shows the recommended way to specify configurations for each sync type\. Please see the *Examples* section when you create your resource data sync\.

## Syntax<a name="aws-resource-ssm-resourcedatasync-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-resourcedatasync-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::ResourceDataSync",
  "Properties" : {
      "[BucketName](#cfn-ssm-resourcedatasync-bucketname)" : String,
      "[BucketPrefix](#cfn-ssm-resourcedatasync-bucketprefix)" : String,
      "[BucketRegion](#cfn-ssm-resourcedatasync-bucketregion)" : String,
      "[KMSKeyArn](#cfn-ssm-resourcedatasync-kmskeyarn)" : String,
      "[S3Destination](#cfn-ssm-resourcedatasync-s3destination)" : S3Destination,
      "[SyncFormat](#cfn-ssm-resourcedatasync-syncformat)" : String,
      "[SyncName](#cfn-ssm-resourcedatasync-syncname)" : String,
      "[SyncSource](#cfn-ssm-resourcedatasync-syncsource)" : SyncSource,
      "[SyncType](#cfn-ssm-resourcedatasync-synctype)" : String
    }
}
```

### YAML<a name="aws-resource-ssm-resourcedatasync-syntax.yaml"></a>

```
Type: AWS::SSM::ResourceDataSync
Properties: 
  [BucketName](#cfn-ssm-resourcedatasync-bucketname): String
  [BucketPrefix](#cfn-ssm-resourcedatasync-bucketprefix): String
  [BucketRegion](#cfn-ssm-resourcedatasync-bucketregion): String
  [KMSKeyArn](#cfn-ssm-resourcedatasync-kmskeyarn): String
  [S3Destination](#cfn-ssm-resourcedatasync-s3destination): 
    S3Destination
  [SyncFormat](#cfn-ssm-resourcedatasync-syncformat): String
  [SyncName](#cfn-ssm-resourcedatasync-syncname): String
  [SyncSource](#cfn-ssm-resourcedatasync-syncsource): 
    SyncSource
  [SyncType](#cfn-ssm-resourcedatasync-synctype): String
```

## Properties<a name="aws-resource-ssm-resourcedatasync-properties"></a>

`BucketName`  <a name="cfn-ssm-resourcedatasync-bucketname"></a>
The name of the S3 bucket where the aggregated data is stored\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketPrefix`  <a name="cfn-ssm-resourcedatasync-bucketprefix"></a>
An Amazon S3 prefix for the bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketRegion`  <a name="cfn-ssm-resourcedatasync-bucketregion"></a>
The AWS Region with the S3 bucket targeted by the Resource Data Sync\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KMSKeyArn`  <a name="cfn-ssm-resourcedatasync-kmskeyarn"></a>
The ARN of an encryption key for a destination in Amazon S3\. You can use a KMS key to encrypt inventory data in Amazon S3\. You must specify a key that exist in the same region as the destination Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3Destination`  <a name="cfn-ssm-resourcedatasync-s3destination"></a>
Configuration information for the target S3 bucket\.  
*Required*: No  
*Type*: [S3Destination](aws-properties-ssm-resourcedatasync-s3destination.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SyncFormat`  <a name="cfn-ssm-resourcedatasync-syncformat"></a>
A supported sync format\. The following format is currently supported: JsonSerDe  
*Required*: No  
*Type*: String  
*Allowed values*: `JsonSerDe`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SyncName`  <a name="cfn-ssm-resourcedatasync-syncname"></a>
A name for the Resource Data Sync\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SyncSource`  <a name="cfn-ssm-resourcedatasync-syncsource"></a>
Information about the source where the data was synchronized\.   
*Required*: No  
*Type*: [SyncSource](aws-properties-ssm-resourcedatasync-syncsource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SyncType`  <a name="cfn-ssm-resourcedatasync-synctype"></a>
The type of resource data sync\. If `SyncType` is `SyncToDestination`, then the resource data sync synchronizes data to an S3 bucket\. If the `SyncType` is `SyncFromSource` then the resource data sync synchronizes data from AWS Organizations or from multiple AWS Regions\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ssm-resourcedatasync-return-values"></a>

### Ref<a name="aws-resource-ssm-resourcedatasync-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the Resource Data Sync, such as `TestResourceDataSync`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ssm-resourcedatasync--examples"></a>

### Create a SyncToDestination Resource Data Sync<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncToDestination_Resource_Data_Sync"></a>

The following example synchronizes Systems Manager Inventory metadata in the US East \(Ohio\) Region \(us\-east\-2\) to a single Amazon S3 bucket\. Resource Data Sync then automatically updates the centralized data when new data is collected\.

#### JSON<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncToDestination_Resource_Data_Sync--json"></a>

```
{
    "Description": "Create a Resource Data Sync for Systems Manager",
    "Resources": {
        "BasicResourceDataSync": {
            "Type": "AWS::SSM::ResourceDataSync",
            "Properties": {
                "SyncName": "test-sync",
                "SyncType": "SyncToDestination",
                "S3Destination": {
                    "BucketName": "test-bucket",
                    "BucketRegion": "us-east-2",
                    "SyncFormat": "JsonSerDe",
                    "BucketPrefix": "cfn",
                    "KMSKeyArn": "kmsKeyARN"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncToDestination_Resource_Data_Sync--yaml"></a>

```
---
Description: Create a Resource Data Sync for Systems Manager
Resources:
  BasicResourceDataSync:
    Type: AWS::SSM::ResourceDataSync
    Properties:
      SyncName: test-sync
      SyncType: SyncToDestination
      S3Destination:
        BucketName: test-bucket
        BucketRegion: us-east-2
        SyncFormat: JsonSerDe
        BucketPrefix: cfn
        KMSKeyArn: kmsKeyARN
```

### Create a SyncFromSource Resource Data Sync with type SingleAccountMultipleRegions<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncFromSource_Resource_Data_Sync_with_type_SingleAccountMultipleRegions"></a>

The following example synchronizes Systems Manager Explorer OpsData and OpsItems from multiple AWS Regions in a single AWS account\.

#### JSON<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncFromSource_Resource_Data_Sync_with_type_SingleAccountMultipleRegions--json"></a>

```
{
    "Description": "Create a Resource Data Sync for Systems Manager Explorer",
    "Resources": {
        "BasicResourceDataSync": {
            "Type": "Dev::SSM::ResourceDataSync",
            "Properties": {
                "SyncName": "test-sync",
                "SyncType": "SyncFromSource",
                "SyncSource": {
                    "SourceType": "SingleAccountMultiRegions",
                    "SourceRegions": [
                        "us-east-1",
                        "us-west-1",
                        "us-west-2"
                    ],
                    "IncludeFutureRegions": false
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncFromSource_Resource_Data_Sync_with_type_SingleAccountMultipleRegions--yaml"></a>

```
---
Description: Create a Resource Data Sync for Systems Manager Explorer
Resources:
  BasicResourceDataSync:
    Type: Dev::SSM::ResourceDataSync
    Properties:
      SyncName: test-sync
      SyncType: SyncFromSource
      SyncSource:
        SourceType: SingleAccountMultiRegions
        SourceRegions:
        - us-east-1
        - us-west-1
        - us-west-2
        IncludeFutureRegions: false
```

### Create a SyncFromSource Resource Data Sync with type EntireOrganization<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncFromSource_Resource_Data_Sync_with_type_EntireOrganization"></a>

The following example synchronizes Systems Manager Explorer OpsData and OpsItems from your entire organization in AWS Organizations in the us\-west\-1 Region\. 

#### JSON<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncFromSource_Resource_Data_Sync_with_type_EntireOrganization--json"></a>

```
{
    "Description": "Create a Resource Data Sync for Systems Manager Explorer",
    "Resources": {
        "BasicResourceDataSync": {
            "Type": "Dev::SSM::ResourceDataSync",
            "Properties": {
                "SyncName": "test-sync",
                "SyncType": "SyncFromSource",
                "SyncSource": {
                    "SourceType": "AwsOrganizations",
                    "AwsOrganizationsSource": {
                        "OrganizationSourceType": "EntireOrganization"
                    },
                    "SourceRegions": [
                        "us-west-1"
                    ],
                    "IncludeFutureRegions": false
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-resourcedatasync--examples--Create_a_SyncFromSource_Resource_Data_Sync_with_type_EntireOrganization--yaml"></a>

```
---
Description: Create a Resource Data Sync for Systems Manager Explorer
Resources:
  BasicResourceDataSync:
    Type: Dev::SSM::ResourceDataSync
    Properties:
      SyncName: test-sync
      SyncType: SyncFromSource
      SyncSource:
        SourceType: AwsOrganizations
        AwsOrganizationsSource:
          OrganizationSourceType: EntireOrganization
        SourceRegions:
        - us-west-1
        IncludeFutureRegions: false
```

### Creating a SyncFromSource Resource Data Sync with type OrganizationalUnits<a name="aws-resource-ssm-resourcedatasync--examples--Creating_a_SyncFromSource_Resource_Data_Sync_with_type_OrganizationalUnits"></a>

The following example synchronizes Systems Manager Explorer OpsData and OpsItems from organization unit 12345 in AWS Organizations in the us\-west\-1 Region\. 

#### JSON<a name="aws-resource-ssm-resourcedatasync--examples--Creating_a_SyncFromSource_Resource_Data_Sync_with_type_OrganizationalUnits--json"></a>

```
{
    "Description": "Create a Resource Data Sync for Systems Manager Explorer",
    "Resources": {
        "BasicResourceDataSync": {
            "Type": "AWS::SSM::ResourceDataSync",
            "Properties": {
                "SyncName": "test-sync",
                "SyncType": "SyncFromSource",
                "SyncSource": {
                    "SourceType": "AwsOrganizations",
                    "AwsOrganizationsSource": {
                        "OrganizationSourceType": "OrganizationalUnits",
                        "OrganizationalUnits": [
                            "ou-12345"
                        ]
                    },
                    "SourceRegions": [
                        "us-west-1"
                    ],
                    "IncludeFutureRegions": false
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-resourcedatasync--examples--Creating_a_SyncFromSource_Resource_Data_Sync_with_type_OrganizationalUnits--yaml"></a>

```
---
Description: Create a Resource Data Sync for Systems Manager Explorer
Resources:
  BasicResourceDataSync:
    Type: AWS::SSM::ResourceDataSync
    Properties:
      SyncName: test-sync
      SyncType: SyncFromSource
      SyncSource:
        SourceType: AwsOrganizations
        AwsOrganizationsSource:
          OrganizationSourceType: OrganizationalUnits
          OrganizationalUnits:
          - ou-12345
        SourceRegions:
        - us-west-1
        IncludeFutureRegions: false
```

## See also<a name="aws-resource-ssm-resourcedatasync--seealso"></a>
+  [What is Systems Manager?](https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html) 
+  [AWS Systems Manager Inventory](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-inventory.html) 
+  [Configuring Inventory Collection](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-inventory-configuring.html) 