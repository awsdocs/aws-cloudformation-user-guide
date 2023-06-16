# AWS::S3::Bucket VersioningConfiguration<a name="aws-properties-s3-bucket-versioningconfiguration"></a>

Describes the versioning state of an Amazon S3 bucket\. For more information, see [PUT Bucket versioning](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTVersioningStatus.html) in the *Amazon S3 API Reference*\.

## Syntax<a name="aws-properties-s3-bucket-versioningconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-versioningconfiguration-syntax.json"></a>

```
{
  "[Status](#cfn-s3-bucket-versioningconfiguration-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-versioningconfiguration-syntax.yaml"></a>

```
  [Status](#cfn-s3-bucket-versioningconfiguration-status): String
```

## Properties<a name="aws-properties-s3-bucket-versioningconfiguration-properties"></a>

`Status`  <a name="cfn-s3-bucket-versioningconfiguration-status"></a>
The versioning state of the bucket\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Enabled | Suspended`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-versioningconfiguration--examples"></a>



### Enable versioning and replicate objects<a name="aws-properties-s3-bucket-versioningconfiguration--examples--Enable_versioning_and_replicate_objects"></a>

The following example enables versioning and two replication rules\. The rules copy objects prefixed with either `MyPrefix` and `MyOtherPrefix` and stores the copied objects in a bucket named `my-replication-bucket`\.

#### JSON<a name="aws-properties-s3-bucket-versioningconfiguration--examples--Enable_versioning_and_replicate_objects--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "VersioningConfiguration": {
                    "Status": "Enabled"
                },
                "ReplicationConfiguration": {
                    "Role": "arn:aws:iam::123456789012:role/replication_role",
                    "Rules": [
                        {
                            "Id": "MyRule1",
                            "Status": "Enabled",
                            "Prefix": "MyPrefix",
                            "Destination": {
                                "Bucket": "arn:aws:s3:::my-replication-bucket",
                                "StorageClass": "STANDARD"
                            }
                        },
                        {
                            "Status": "Enabled",
                            "Prefix": "MyOtherPrefix",
                            "Destination": {
                                "Bucket": "arn:aws:s3:::my-replication-bucket"
                            }
                        }
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-versioningconfiguration--examples--Enable_versioning_and_replicate_objects--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      VersioningConfiguration:
        Status: Enabled
      ReplicationConfiguration:
        Role: 'arn:aws:iam::123456789012:role/replication_role'
        Rules:
          - Id: MyRule1
            Status: Enabled
            Prefix: MyPrefix
            Destination:
              Bucket: 'arn:aws:s3:::my-replication-bucket'
              StorageClass: STANDARD
          - Status: Enabled
            Prefix: MyOtherPrefix
            Destination:
              Bucket: 'arn:aws:s3:::my-replication-bucket'
```