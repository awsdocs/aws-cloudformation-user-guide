# AWS::S3Outposts::Bucket<a name="aws-resource-s3outposts-bucket"></a>

The AWS::S3Outposts::Bucket resource specifies a new Amazon S3 on Outposts bucket\. To create an S3 on Outposts bucket, you must have S3 on Outposts capacity provisioned on your Outpost\. For more information, see [ Using Amazon S3 on Outposts](https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html)\.

S3 on Outposts buckets support the following:
+ Tags
+ Lifecycle configuration rules for deleting expired objects

For a complete list of restrictions and Amazon S3 feature limitations on S3 on Outposts, see [ Amazon S3 on Outposts Restrictions and Limitations](https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3OnOutpostsRestrictionsLimitations.html)\.

## Syntax<a name="aws-resource-s3outposts-bucket-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3outposts-bucket-syntax.json"></a>

```
{
  "Type" : "AWS::S3Outposts::Bucket",
  "Properties" : {
      "[BucketName](#cfn-s3outposts-bucket-bucketname)" : String,
      "[LifecycleConfiguration](#cfn-s3outposts-bucket-lifecycleconfiguration)" : LifecycleConfiguration,
      "[OutpostId](#cfn-s3outposts-bucket-outpostid)" : String,
      "[Tags](#cfn-s3outposts-bucket-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-s3outposts-bucket-syntax.yaml"></a>

```
Type: AWS::S3Outposts::Bucket
Properties: 
  [BucketName](#cfn-s3outposts-bucket-bucketname): String
  [LifecycleConfiguration](#cfn-s3outposts-bucket-lifecycleconfiguration): 
    LifecycleConfiguration
  [OutpostId](#cfn-s3outposts-bucket-outpostid): String
  [Tags](#cfn-s3outposts-bucket-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-s3outposts-bucket-properties"></a>

`BucketName`  <a name="cfn-s3outposts-bucket-bucketname"></a>
A name for the S3 on Outposts bucket\. If you don't specify a name, AWS CloudFormation generates a unique ID and uses that ID for the bucket name\. The bucket name must contain only lowercase letters, numbers, periods \(\.\), and dashes \(\-\) and must follow [ Amazon S3 bucket restrictions and limitations](https://docs.aws.amazon.com/AmazonS3/latest/userguide/BucketRestrictions.html)\. For more information, see [Bucket naming rules](https://docs.aws.amazon.com/AmazonS3/latest/userguide/BucketRestrictions.html#bucketnamingrules)\.   
If you specify a name, you can't perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you need to replace the resource, specify a new name\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LifecycleConfiguration`  <a name="cfn-s3outposts-bucket-lifecycleconfiguration"></a>
Creates a new lifecycle configuration for the S3 on Outposts bucket or replaces an existing lifecycle configuration\. Outposts buckets only support lifecycle configurations that delete/expire objects after a certain period of time and abort incomplete multipart uploads\.  
*Required*: No  
*Type*: [LifecycleConfiguration](aws-properties-s3outposts-bucket-lifecycleconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutpostId`  <a name="cfn-s3outposts-bucket-outpostid"></a>
The ID of the Outpost of the specified bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-s3outposts-bucket-tags"></a>
Sets the tags for an S3 on Outposts bucket\. For more information, see [Using Amazon S3 on Outposts](https://docs.aws.amazon.com/AmazonS3/latest/userguide/S3onOutposts.html)\.  
Use tags to organize your AWS bill to reflect your own cost structure\. To do this, sign up to get your AWS account bill with tag key values included\. Then, to see the cost of combined resources, organize your billing information according to resources with the same tag key values\. For example, you can tag several resources with a specific application name, and then organize your billing information to see the total cost of that application across several services\. For more information, see [Cost allocation and tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html)\.  
Within a bucket, if you add a tag that has the same key as an existing tag, the new value overwrites the old value\. For more information, see [ Using cost allocation and bucket tags](https://docs.aws.amazon.com/AmazonS3/latest/userguide/CostAllocTagging.html)\.
To use this resource, you must have permissions to perform the `s3-outposts:PutBucketTagging`\. The S3 on Outposts bucket owner has this permission by default and can grant this permission to others\. For more information about permissions, see [Permissions Related to Bucket Subresource Operations](https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-with-s3-actions.html#using-with-s3-actions-related-to-bucket-subresources) and [Managing access permissions to your Amazon S3 resources](https://docs.aws.amazon.com/AmazonS3/latest/userguide/s3-access-control.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-s3outposts-bucket-return-values"></a>

### Ref<a name="aws-resource-s3outposts-bucket-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the S3 on Outposts bucket Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3outposts-bucket-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-s3outposts-bucket-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the ARN of the specified bucket\.  
Example: `arn:aws:s3Outposts:::DOC-EXAMPLE-BUCKET` 

## Examples<a name="aws-resource-s3outposts-bucket--examples"></a>

The following examples create an Amazon S3 on Outposts bucket using AWS CloudFormation\.

### Create an S3 on Outposts bucket<a name="aws-resource-s3outposts-bucket--examples--Create_an_S3_on_Outposts_bucket"></a>

The following example creates an S3 on Outposts bucket without tags or lifecycle configuration\.

#### JSON<a name="aws-resource-s3outposts-bucket--examples--Create_an_S3_on_Outposts_bucket--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Bucket, no tags, no lifecycle configuration",
    "Resources": {
        "ExampleS3OutpostsBucket": {
            "Type": "AWS::S3Outposts::Bucket",
            "Properties": {
                "BucketName": "DOC-EXAMPLE-BUCKET",
                "OutpostID": "op-01ac5d28a6a232904"
            }
        }
    },
    "Outputs": {
        "ExampleS3OutpostsBucketARN": {
            "Description": "The ARN of ExampleS3OutpostsBucket",
            "Value": {
                "Ref": "ExampleS3OutpostsBucket"
            }
        },
        "ExampleS3OutpostsStackID": {
            "Description": "The stack ID",
            "Value": {
                "Ref": "AWS::StackID"
            },
            "Export": {
                "Name": {
                    "Fn::Sub": "${AWS::StackName}-StackID"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-s3outposts-bucket--examples--Create_an_S3_on_Outposts_bucket--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Bucket, no tags, no lifecycle configuration
Resources:
  ExampleS3OutpostsBucket:
    Type: AWS::S3Outposts::Bucket
    Properties:
      BucketName: DOC-EXAMPLE-BUCKET
      OutpostID: op-01ac5d28a6a232904
Outputs:
  ExampleS3OutpostsBucketARN:
    Description: The ARN of ExampleS3OutpostsBucket
    Value:
      Ref: ExampleS3OutpostsBucket
  ExampleS3OutpostsStackID:
    Description: The stack ID
    Value:
      Ref: AWS::StackID
    Export:
      Name:
        Fn::Sub: "${AWS::StackName}-StackID"
```

### Creates an S3 on Outposts bucket with tags<a name="aws-resource-s3outposts-bucket--examples--Creates_an_S3_on_Outposts_bucket_with_tags"></a>

The following example creates an S3 on Outposts bucket with tags and no lifecycle configuration\.

#### JSON<a name="aws-resource-s3outposts-bucket--examples--Creates_an_S3_on_Outposts_bucket_with_tags--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Bucket, tags, no lifecycle configuration",
    "Resources": {
        "ExampleS3OutpostsBucket": {
            "Type": "AWS::S3Outposts::Bucket",
            "Properties": {
                "BucketName": "DOC-EXAMPLE-BUCKET",
                "OutpostID": "op-01ac5d28a6a232904",
                "Tags": [
                    {
                        "Key": "stage",
                        "Value": "beta"
                    },
                    {
                        "Key": "purpose",
                        "Value": "testing"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "ExampleS3OutpostsBucketARN": {
            "Description": "The ARN of ExampleS3OutpostsBucket",
            "Value": {
                "Ref": "ExampleS3OutpostsBucket"
            }
        },
        "ExampleS3OutpostsStackID": {
            "Description": "The stack ID",
            "Value": {
                "Ref": "AWS::StackID"
            },
            "Export": {
                "Name": {
                    "Fn::Sub": "${AWS::StackName}-StackID"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-s3outposts-bucket--examples--Creates_an_S3_on_Outposts_bucket_with_tags--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Bucket, tags, no lifecycle configuration
Resources:
  ExampleS3OutpostsBucket:
    Type: AWS::S3Outposts::Bucket
    Properties:
      BucketName: DOC-EXAMPLE-BUCKET
      OutpostID: op-01ac5d28a6a232904
      Tags:
      - Key: stage
        Value: beta
      - Key: purpose
        Value: testing
Outputs:
  ExampleS3OutpostsBucketARN:
    Description: The ARN of ExampleS3OutpostsBucket
    Value:
      Ref: ExampleS3OutpostsBucket
  ExampleS3OutpostsStackID:
    Description: The stack ID
    Value:
      Ref: AWS::StackID
    Export:
      Name:
        Fn::Sub: "${AWS::StackName}-StackID"
```

### Creates an S3 on Outposts bucket with tags and lifecycle configuration<a name="aws-resource-s3outposts-bucket--examples--Creates_an_S3_on_Outposts_bucket_with_tags_and_lifecycle_configuration"></a>

The following example creates an S3 on Outposts bucket with tags and four lifecycle configuration rules\. Three of the four lifecycle rules are disabled\.

**Note**  
All lifecycle rules must have values for either `ExpirationInDays`, `ExpirationDate`, or `DaysAfterInitiation` for `AbortIncompleteMultipartUpload` to be valid\.

#### JSON<a name="aws-resource-s3outposts-bucket--examples--Creates_an_S3_on_Outposts_bucket_with_tags_and_lifecycle_configuration--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Bucket, tags, lifecycle configuration",
    "Resources": {
        "ExampleS3OutpostsBucket": {
            "Type": "AWS::S3Outposts::Bucket",
            "Properties": {
                "BucketName": "DOC-EXAMPLE-BUCKET",
                "OutpostID": "op-01ac5d28a6a232904",
                "Tags": [
                    {
                        "Key": "stage",
                        "Value": "beta"
                    },
                    {
                        "Key": "purpose",
                        "Value": "testing"
                    }
                ],
                "LifecycleConfiguration": {
                    "Rules": [
                        {
                            "ExpirationInDays": 2,
                            "ID": "rule1",
                            "Status": "Enabled"
                        },
                        {
                            "AbortIncompleteMultipartUpload": {
                                "DaysAfterInitiation": 2
                            },
                            "ID": "rule2",
                            "Status": "Disabled",
                            "Filter": {
                                "AndOperator": {
                                    "Prefix": "st",
                                    "Tags": [
                                        {
                                            "Key": "purpose",
                                            "Value": "testing"
                                        }
                                    ]
                                }
                            }
                        },
                        {
                            "ExpirationDate": "2020-02-25T00:00:00Z",
                            "ID": "rule3",
                            "Status": "Disabled",
                            "Filter": {
                                "Tag": {
                                    "Key": "stage",
                                    "Value": "beta"
                                }
                            }
                        },
                        {
                            "ExpirationInDays": 4,
                            "ID": "rule4",
                            "Status": "Disabled",
                            "Filter": {
                                "Prefix": "st"
                            }
                        }
                    ]
                }
            }
        }
    },
    "Outputs": {
        "ExampleS3OutpostsBucketARN": {
            "Description": "The ARN of ExampleS3OutpostsBucket",
            "Value": {
                "Ref": "ExampleS3OutpostsBucket"
            }
        },
        "ExampleStackID": {
            "Description": "The stack ID",
            "Value": {
                "Ref": "AWS::StackID"
            },
            "Export": {
                "Name": {
                    "Fn::Sub": "${AWS::StackName}-StackID"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-s3outposts-bucket--examples--Creates_an_S3_on_Outposts_bucket_with_tags_and_lifecycle_configuration--yaml"></a>

```
---
AWSTemplateFormatVersion: '2010-09-09'
Description: Bucket, tags, lifecycle configuration
Resources:
  ExampleS3OutpostsBucket:
    Type: AWS::S3Outposts::Bucket
    Properties:
      BucketName: DOC-EXAMPLE-BUCKET
      OutpostID: op-01ac5d28a6a232904
      Tags:
      - Key: stage
        Value: beta
      - Key: purpose
        Value: testing
      LifecycleConfiguration:
        Rules:
        - ExpirationInDays: 2
          ID: rule1
          Status: Enabled
        - AbortIncompleteMultipartUpload:
            DaysAfterInitiation: 2
          ID: rule2
          Status: Disabled
          Filter:
            AndOperator:
              Prefix: st
              Tags:
              - Key: purpose
                Value: testing
        - ExpirationDate: '2020-02-25T00:00:00Z'
          ID: rule3
          Status: Disabled
          Filter:
            Tag:
              Key: stage
              Value: beta
        - ExpirationInDays: 4
          ID: rule4
          Status: Disabled
          Filter:
            Prefix: st
Outputs:
  ExampleS3OutpostsBucketARN:
    Description: The ARN of ExampleS3OutpostsBucket
    Value:
      Ref: ExampleS3OutpostsBucket
  ExampleStackID:
    Description: The stack ID
    Value:
      Ref: AWS::StackID
    Export:
      Name:
        Fn::Sub: "${AWS::StackName}-StackID"
```