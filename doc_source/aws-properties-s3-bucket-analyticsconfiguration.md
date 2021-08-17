# AWS::S3::Bucket AnalyticsConfiguration<a name="aws-properties-s3-bucket-analyticsconfiguration"></a>

Specifies the configuration and any analyses for the analytics filter of an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-bucket-analyticsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-analyticsconfiguration-syntax.json"></a>

```
{
  "[Id](#cfn-s3-bucket-analyticsconfiguration-id)" : String,
  "[Prefix](#cfn-s3-bucket-analyticsconfiguration-prefix)" : String,
  "[StorageClassAnalysis](#cfn-s3-bucket-analyticsconfiguration-storageclassanalysis)" : StorageClassAnalysis,
  "[TagFilters](#cfn-s3-bucket-analyticsconfiguration-tagfilters)" : [ TagFilter, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-analyticsconfiguration-syntax.yaml"></a>

```
  [Id](#cfn-s3-bucket-analyticsconfiguration-id): String
  [Prefix](#cfn-s3-bucket-analyticsconfiguration-prefix): String
  [StorageClassAnalysis](#cfn-s3-bucket-analyticsconfiguration-storageclassanalysis): 
    StorageClassAnalysis
  [TagFilters](#cfn-s3-bucket-analyticsconfiguration-tagfilters): 
    - TagFilter
```

## Properties<a name="aws-properties-s3-bucket-analyticsconfiguration-properties"></a>

`Id`  <a name="cfn-s3-bucket-analyticsconfiguration-id"></a>
The ID that identifies the analytics configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-analyticsconfiguration-prefix"></a>
The prefix that an object must have to be included in the analytics results\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageClassAnalysis`  <a name="cfn-s3-bucket-analyticsconfiguration-storageclassanalysis"></a>
 Contains data related to access patterns to be collected and made available to analyze the tradeoffs between different storage classes\.   
*Required*: Yes  
*Type*: [StorageClassAnalysis](aws-properties-s3-bucket-storageclassanalysis.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagFilters`  <a name="cfn-s3-bucket-analyticsconfiguration-tagfilters"></a>
The tags to use when evaluating an analytics filter\.  
The analytics only includes objects that meet the filter's criteria\. If no filter is specified, all of the contents of the bucket are included in the analysis\.  
*Required*: No  
*Type*: List of [TagFilter](aws-properties-s3-bucket-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-analyticsconfiguration--examples"></a>



### Specify analytics and inventory configurations for an S3 bucket<a name="aws-properties-s3-bucket-analyticsconfiguration--examples--Specify_analytics_and_inventory_configurations_for_an_S3_bucket"></a>

The following example specifies analytics and inventory results to be generated for an S3 bucket, including the format of the results and the destination bucket\. The inventory list generates reports weekly and includes the current version of each object\.

#### JSON<a name="aws-properties-s3-bucket-analyticsconfiguration--examples--Specify_analytics_and_inventory_configurations_for_an_S3_bucket--json"></a>

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

#### YAML<a name="aws-properties-s3-bucket-analyticsconfiguration--examples--Specify_analytics_and_inventory_configurations_for_an_S3_bucket--yaml"></a>

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