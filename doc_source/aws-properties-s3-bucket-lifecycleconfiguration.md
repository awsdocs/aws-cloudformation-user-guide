# AWS::S3::Bucket LifecycleConfiguration<a name="aws-properties-s3-bucket-lifecycleconfiguration"></a>

Specifies the lifecycle configuration for objects in an Amazon S3 bucket\. For more information, see [Object Lifecycle Management](https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-bucket-lifecycleconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-lifecycleconfiguration-syntax.json"></a>

```
{
  "[Rules](#cfn-s3-bucket-lifecycleconfiguration-rules)" : [ Rule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-lifecycleconfiguration-syntax.yaml"></a>

```
  [Rules](#cfn-s3-bucket-lifecycleconfiguration-rules): 
    - Rule
```

## Properties<a name="aws-properties-s3-bucket-lifecycleconfiguration-properties"></a>

`Rules`  <a name="cfn-s3-bucket-lifecycleconfiguration-rules"></a>
A lifecycle rule for individual objects in an Amazon S3 bucket\.  
*Required*: Yes  
*Type*: List of [Rule](aws-properties-s3-bucket-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-lifecycleconfiguration--examples"></a>



### Manage the lifecycle for S3 objects<a name="aws-properties-s3-bucket-lifecycleconfiguration--examples--Manage_the_lifecycle_for_S3_objects"></a>

The following example template shows an S3 bucket with a lifecycle configuration rule\. The rule applies to all objects with the `glacier` key prefix\. The objects are transitioned to Glacier after one day, and deleted after one year\.

#### JSON<a name="aws-properties-s3-bucket-lifecycleconfiguration--examples--Manage_the_lifecycle_for_S3_objects--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "Private",
                "LifecycleConfiguration": {
                    "Rules": [
                        {
                            "Id": "GlacierRule",
                            "Prefix": "glacier",
                            "Status": "Enabled",
                            "ExpirationInDays": 365,
                            "Transitions": [
                                {
                                    "TransitionInDays": 1,
                                    "StorageClass": "GLACIER"
                                }
                            ]
                        }
                    ]
                }
            }
        }
    },
    "Outputs": {
        "BucketName": {
            "Value": {
                "Ref": "S3Bucket"
            },
            "Description": "Name of the sample Amazon S3 bucket with a lifecycle configuration."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-lifecycleconfiguration--examples--Manage_the_lifecycle_for_S3_objects--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: Private
      LifecycleConfiguration:
        Rules:
          - Id: GlacierRule
            Prefix: glacier
            Status: Enabled
            ExpirationInDays: 365
            Transitions:
              - TransitionInDays: 1
                StorageClass: GLACIER
Outputs:
  BucketName:
    Value: !Ref S3Bucket
    Description: Name of the sample Amazon S3 bucket with a lifecycle configuration.
```