# AWS::S3::Bucket InventoryConfiguration<a name="aws-properties-s3-bucket-inventoryconfiguration"></a>

Specifies the inventory configuration for an Amazon S3 bucket\. For more information, see [GET Bucket inventory](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketGETInventoryConfig.html) in the *Amazon S3 API Reference*\. 

## Syntax<a name="aws-properties-s3-bucket-inventoryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-inventoryconfiguration-syntax.json"></a>

```
{
  "[Destination](#cfn-s3-bucket-inventoryconfiguration-destination)" : Destination,
  "[Enabled](#cfn-s3-bucket-inventoryconfiguration-enabled)" : Boolean,
  "[Id](#cfn-s3-bucket-inventoryconfiguration-id)" : String,
  "[IncludedObjectVersions](#cfn-s3-bucket-inventoryconfiguration-includedobjectversions)" : String,
  "[OptionalFields](#cfn-s3-bucket-inventoryconfiguration-optionalfields)" : [ String, ... ],
  "[Prefix](#cfn-s3-bucket-inventoryconfiguration-prefix)" : String,
  "[ScheduleFrequency](#cfn-s3-bucket-inventoryconfiguration-schedulefrequency)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-inventoryconfiguration-syntax.yaml"></a>

```
  [Destination](#cfn-s3-bucket-inventoryconfiguration-destination): 
    Destination
  [Enabled](#cfn-s3-bucket-inventoryconfiguration-enabled): Boolean
  [Id](#cfn-s3-bucket-inventoryconfiguration-id): String
  [IncludedObjectVersions](#cfn-s3-bucket-inventoryconfiguration-includedobjectversions): String
  [OptionalFields](#cfn-s3-bucket-inventoryconfiguration-optionalfields): 
    - String
  [Prefix](#cfn-s3-bucket-inventoryconfiguration-prefix): String
  [ScheduleFrequency](#cfn-s3-bucket-inventoryconfiguration-schedulefrequency): String
```

## Properties<a name="aws-properties-s3-bucket-inventoryconfiguration-properties"></a>

`Destination`  <a name="cfn-s3-bucket-inventoryconfiguration-destination"></a>
Contains information about where to publish the inventory results\.  
*Required*: Yes  
*Type*: [Destination](aws-properties-s3-bucket-destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-s3-bucket-inventoryconfiguration-enabled"></a>
Specifies whether the inventory is enabled or disabled\. If set to `True`, an inventory list is generated\. If set to `False`, no inventory list is generated\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3-bucket-inventoryconfiguration-id"></a>
The ID used to identify the inventory configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludedObjectVersions`  <a name="cfn-s3-bucket-inventoryconfiguration-includedobjectversions"></a>
Object versions to include in the inventory list\. If set to `All`, the list includes all the object versions, which adds the version\-related fields `VersionId`, `IsLatest`, and `DeleteMarker` to the list\. If set to `Current`, the list does not contain these version\-related fields\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `All | Current`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionalFields`  <a name="cfn-s3-bucket-inventoryconfiguration-optionalfields"></a>
Contains the optional fields that are included in the inventory results\.  
*Valid values*: ` Size | LastModifiedDate | StorageClass | ETag | IsMultipartUploaded | ReplicationStatus | EncryptionStatus | ObjectLockRetainUntilDate | ObjectLockMode | ObjectLockLegalHoldStatus | IntelligentTieringAccessTier | BucketKeyStatus `   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-inventoryconfiguration-prefix"></a>
Specifies the inventory filter prefix\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleFrequency`  <a name="cfn-s3-bucket-inventoryconfiguration-schedulefrequency"></a>
Specifies the schedule for generating inventory results\.  
*Allowed values*: `Daily` \| `Weekly`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-inventoryconfiguration--examples"></a>



### Specify analytics and inventory configurations for an S3 bucket<a name="aws-properties-s3-bucket-inventoryconfiguration--examples--Specify_analytics_and_inventory_configurations_for_an_S3_bucket"></a>

The following example specifies analytics and inventory results to be generated for an S3 bucket, including the format of the results and the destination bucket\. The inventory list generates reports weekly and includes the current version of each object\.

#### JSON<a name="aws-properties-s3-bucket-inventoryconfiguration--examples--Specify_analytics_and_inventory_configurations_for_an_S3_bucket--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "S3 Bucket with Inventory and Analytics Configurations",
    "Resources": {
        "Helper": {
            "Type": "AWS::S3::Bucket"
        },
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AnalyticsConfigurations": [
                    {
                        "Id": "AnalyticsConfigurationId",
                        "StorageClassAnalysis": {
                            "DataExport": {
                                "Destination": {
                                    "BucketArn": {
                                        "Fn::GetAtt": [
                                            "Helper",
                                            "Arn"
                                        ]
                                    },
                                    "Format": "CSV",
                                    "Prefix": "AnalyticsDestinationPrefix"
                                },
                                "OutputSchemaVersion": "V_1"
                            }
                        },
                        "Prefix": "AnalyticsConfigurationPrefix",
                        "TagFilters": [
                            {
                                "Key": "AnalyticsTagKey",
                                "Value": "AnalyticsTagValue"
                            }
                        ]
                    }
                ],
                "InventoryConfigurations": [
                    {
                        "Id": "InventoryConfigurationId",
                        "Destination": {
                            "BucketArn": {
                                "Fn::GetAtt": [
                                    "Helper",
                                    "Arn"
                                ]
                            },
                            "Format": "CSV",
                            "Prefix": "InventoryDestinationPrefix"
                        },
                        "Enabled": true,
                        "IncludedObjectVersions": "Current",
                        "Prefix": "InventoryConfigurationPrefix",
                        "ScheduleFrequency": "Weekly"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-inventoryconfiguration--examples--Specify_analytics_and_inventory_configurations_for_an_S3_bucket--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: S3 Bucket with Inventory and Analytics Configurations
Resources:
  Helper:
    Type: 'AWS::S3::Bucket'
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AnalyticsConfigurations:
        - Id: AnalyticsConfigurationId
          StorageClassAnalysis:
            DataExport:
              Destination:
                BucketArn: !GetAtt
                  - Helper
                  - Arn
                Format: CSV
                Prefix: AnalyticsDestinationPrefix
              OutputSchemaVersion: V_1
          Prefix: AnalyticsConfigurationPrefix
          TagFilters:
            - Key: AnalyticsTagKey
              Value: AnalyticsTagValue
      InventoryConfigurations:
        - Id: InventoryConfigurationId
          Destination:
            BucketArn: !GetAtt
              - Helper
              - Arn
            Format: CSV
            Prefix: InventoryDestinationPrefix
          Enabled: true
          IncludedObjectVersions: Current
          Prefix: InventoryConfigurationPrefix
          ScheduleFrequency: Weekly
```