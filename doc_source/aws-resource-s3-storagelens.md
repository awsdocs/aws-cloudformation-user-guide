# AWS::S3::StorageLens<a name="aws-resource-s3-storagelens"></a>

The AWS::S3::StorageLens resource creates an Amazon S3 Storage Lens configuration\.

## Syntax<a name="aws-resource-s3-storagelens-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3-storagelens-syntax.json"></a>

```
{
  "Type" : "AWS::S3::StorageLens",
  "Properties" : {
      "[StorageLensConfiguration](#cfn-s3-storagelens-storagelensconfiguration)" : StorageLensConfiguration,
      "[Tags](#cfn-s3-storagelens-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-s3-storagelens-syntax.yaml"></a>

```
Type: AWS::S3::StorageLens
Properties: 
  [StorageLensConfiguration](#cfn-s3-storagelens-storagelensconfiguration): 
    StorageLensConfiguration
  [Tags](#cfn-s3-storagelens-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-s3-storagelens-properties"></a>

`StorageLensConfiguration`  <a name="cfn-s3-storagelens-storagelensconfiguration"></a>
This resource contains the details Amazon S3 Storage Lens configuration\.  
*Required*: Yes  
*Type*: [StorageLensConfiguration](aws-properties-s3-storagelens-storagelensconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-s3-storagelens-tags"></a>
A set of tags \(key–value pairs\) to associate with the Storage Lens configuration\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-s3-storagelens-return-values"></a>

### Ref<a name="aws-resource-s3-storagelens-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the S3 Storage Lens configuration Id, such as `your-storage-lens-configuration-id`\. For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3-storagelens-return-values-fn--getatt"></a>

Fn::GetAtt returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-s3-storagelens-return-values-fn--getatt-fn--getatt"></a>

`StorageLensConfiguration.StorageLensArn`  <a name="StorageLensConfiguration.StorageLensArn-fn::getatt"></a>
This property contains the details of the ARN of the S3 Storage Lens configuration\. This property is read\-only\.

## Examples<a name="aws-resource-s3-storagelens--examples"></a>

The following examples create an advanced S3 Storage Lens configuration that enables advanced metrics, Amazon CloudWatch publishing, and prefix aggregation\. This example also configures a metrics export and adds tags\.

### Creating an advanced S3 Storage Lens configuration<a name="aws-resource-s3-storagelens--examples--Creating_an_advanced_S3_Storage_Lens_configuration"></a>

#### JSON<a name="aws-resource-s3-storagelens--examples--Creating_an_advanced_S3_Storage_Lens_configuration--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "StorageLens Advanced Configuration Example",
    "Resources": {
        "StorageLensConfigurationExample": {
            "Type": "AWS::S3::StorageLens",
            "Properties": {
                "StorageLensConfiguration": {
                    "Id": "StorageLensAdvancedConfiguration",
                    "AccountLevel": {
                        "ActivityMetrics": {
                            "IsEnabled": true
                        },
                        "AdvancedCostOptimizationMetrics": {
                            "IsEnabled": true
                        },
                        "AdvancedDataProtectionMetrics": {
                            "IsEnabled": true
                        },
                        "DetailedStatusCodesMetrics": {
                            "IsEnabled": true
                        },
                        "BucketLevel": {
                            "ActivityMetrics": {
                                "IsEnabled": true
                            },
                            "AdvancedCostOptimizationMetrics": {
                                "IsEnabled": true
                            },
                            "AdvancedDataProtectionMetrics": {
                                "IsEnabled": true
                            },
                            "DetailedStatusCodesMetrics": {
                                "IsEnabled": true
                            },
                            "PrefixLevel": {
                                "StorageMetrics": {
                                    "IsEnabled": true,
                                    "SelectionCriteria": {
                                        "MaxDepth": 5,
                                        "MinStorageBytesPercentage": 1.23,
                                        "Delimiter": "/"
                                    }
                                }
                            }
                        }
                    },
                    "Exclude": {
                        "Buckets": [
                            {
                                "Fn::Sub": "arn:aws:s3:::source_bucket_1"
                            },
                            {
                                "Fn::Sub": "arn:aws:s3:::source_bucket_2"
                            }
                        ]
                    },
                    "IsEnabled": true,
                    "DataExport": {
                        "S3BucketDestination": {
                            "OutputSchemaVersion": "V_1",
                            "Format": "CSV",
                            "AccountId": "111122223333",
                            "Arn": {
                                "Fn::Sub": "arn:aws:s3:::destination_bucket"
                            },
                            "Prefix": "output-path-prefix",
                            "Encryption": {
                                "SSES3": {}
                            }
                        },
                        "CloudWatchMetrics": {
                            "IsEnabled": true
                        }
                    }
                },
                "Tags": [
                    {
                        "Key": "tag-key-1",
                        "Value": "tag-value-1"
                    },
                    {
                        "Key": "tag-key-2",
                        "Value": "tag-value-2"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-s3-storagelens--examples--Creating_an_advanced_S3_Storage_Lens_configuration--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: StorageLens Advanced Configuration Example
Resources:
  StorageLensConfigurationExample:
    Type: AWS::S3::StorageLens
    Properties:
      StorageLensConfiguration:
        Id: "StorageLensAdvancedConfiguration"
        AccountLevel:
          ActivityMetrics:
            IsEnabled: true
          AdvancedCostOptimizationMetrics:
            IsEnabled: true
          AdvancedDataProtectionMetrics:
            IsEnabled: true
          DetailedStatusCodesMetrics:
            IsEnabled: true
          BucketLevel:
            ActivityMetrics:
              IsEnabled: true
            AdvancedCostOptimizationMetrics:
              IsEnabled: true
            AdvancedDataProtectionMetrics:
              IsEnabled: true
            DetailedStatusCodesMetrics:
              IsEnabled: true
            PrefixLevel:
              StorageMetrics:
                IsEnabled: true
                SelectionCriteria:
                  MaxDepth: 5
                  MinStorageBytesPercentage: 1.23
                  Delimiter: "/"
        Exclude:
           Buckets:
            - !Sub 'arn:aws:s3:::source_bucket_1'
            - !Sub 'arn:aws:s3:::source_bucket_2'
        IsEnabled: true
        DataExport:
          S3BucketDestination:
            OutputSchemaVersion: "V_1"
            Format: "CSV"
            AccountId: "111122223333"
            Arn: !Sub 'arn:aws:s3:::destination_bucket'
            Prefix: "output-path-prefix"
            Encryption:
              SSES3: {}
          CloudWatchMetrics:
            IsEnabled: true
      Tags:
        - Key: "tag-key-1"
          Value: "tag-value-1"
        - Key: "tag-key-2"
          Value: "tag-value-2"
```