# AWS::S3Outposts::BucketPolicy<a name="aws-resource-s3outposts-bucketpolicy"></a>

This resource applies a bucket policy to an Amazon S3 on Outposts bucket\. 

If you are using an identity other than the root user of the AWS account that owns the S3 on Outposts bucket, the calling identity must have the `s3-outposts:PutBucketPolicy` permissions on the specified Outposts bucket and belong to the bucket owner's account in order to use this resource\. 

If you don't have `s3-outposts:PutBucketPolicy` permissions, S3 on Outposts returns a `403 Access Denied` error\. 

**Important**  
The root user of the AWS account that owns an Outposts bucket can *always* use this resource, even if the policy explicitly denies the root user the ability to perform actions on this resource\. 

 For more information, see the AWS::IAM::Policy [ PolicyDocument](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-policy.html#cfn-iam-policy-policydocument) resource description in this guide and [ Access Policy Language Overview](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-policy-language-overview.html)\.

## Syntax<a name="aws-resource-s3outposts-bucketpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3outposts-bucketpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::S3Outposts::BucketPolicy",
  "Properties" : {
      "[Bucket](#cfn-s3outposts-bucketpolicy-bucket)" : String,
      "[PolicyDocument](#cfn-s3outposts-bucketpolicy-policydocument)" : Json
    }
}
```

### YAML<a name="aws-resource-s3outposts-bucketpolicy-syntax.yaml"></a>

```
Type: AWS::S3Outposts::BucketPolicy
Properties: 
  [Bucket](#cfn-s3outposts-bucketpolicy-bucket): String
  [PolicyDocument](#cfn-s3outposts-bucketpolicy-policydocument): Json
```

## Properties<a name="aws-resource-s3outposts-bucketpolicy-properties"></a>

`Bucket`  <a name="cfn-s3outposts-bucketpolicy-bucket"></a>
The name of the Amazon S3 Outposts bucket to which the policy applies\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyDocument`  <a name="cfn-s3outposts-bucketpolicy-policydocument"></a>
 A policy document containing permissions to add to the specified bucket\. In IAM, you must provide policy documents in JSON format\. However, in CloudFormation, you can provide the policy in JSON or YAML format because CloudFormation converts YAML to JSON before submitting it to IAM\. For more information, see the AWS::IAM::Policy [ PolicyDocument](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-policy.html#cfn-iam-policy-policydocument) resource description in this guide and [ Access Policy Language Overview](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-policy-language-overview.html)\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-s3outposts-bucketpolicy-return-values"></a>

### Ref<a name="aws-resource-s3outposts-bucketpolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the S3 on Outposts bucket Amazon Resource Name \(ARN\)\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-s3outposts-bucketpolicy--examples"></a>

### Create an Amazon S3 on Outposts bucket with a bucket policy<a name="aws-resource-s3outposts-bucketpolicy--examples--Create_an_Amazon_S3_on_Outposts_bucket_with_a_bucket_policy"></a>

The following example creates an Amazon S3 on Outposts bucket and adds a bucket policy to that bucket\.

**Note**  
To add a bucket policy to a bucket, you must create your Outposts bucket before or at the same time as you add your bucket policy\.

#### JSON<a name="aws-resource-s3outposts-bucketpolicy--examples--Create_an_Amazon_S3_on_Outposts_bucket_with_a_bucket_policy--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Bucket with no tags + Bucket Policy",
    "Resources": {
        "ExampleS3OutpostsBucket": {
            "Type": "AWS::S3Outposts::Bucket",
            "Properties": {
                "BucketName": "DOC-EXAMPLE-BUCKET",
                "OutpostID": "op-01ac5d28a6a232904"
            }
        },
        "ExampleS3OutpostsBucketPolicy": {
            "Type": "AWS::S3Outposts::BucketPolicy",
            "Properties": {
                "Bucket": {
                    "Ref": "ExampleS3OutpostsBucket"
                },
                "PolicyDocument": {
                    "Version": "2012-10-17",
                    "ID": "BucketPolicy",
                    "Statement": [
                        {
                            "Sid": "st1",
                            "Effect": "Allow",
                            "Principal": {
                                "AWS": "arn:aws:iam::123456789012:root"
                            },
                            "Action": "s3-outposts:*",
                            "Resource": "arn:aws:s3-outposts:us-east-1:123456789012:outpost/op-01ac5d28a6a232904/bucket/DOC-EXAMPLE-BUCKET"
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
        "ExampleS3OutpostsBucketPolicyARN": {
            "Description": "The ARN of the BucketPolicy",
            "Value": {
                "Ref": "ExampleS3OutpostsBucketPolicy"
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

#### YAML<a name="aws-resource-s3outposts-bucketpolicy--examples--Create_an_Amazon_S3_on_Outposts_bucket_with_a_bucket_policy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Bucket with no tags + Bucket Policy
Resources:
  ExampleS3OutpostsBucket:
    Type: 'AWS::S3Outposts::Bucket'
    Properties:
      BucketName: DOC-EXAMPLE-BUCKET
      OutpostID: op-01ac5d28a6a232904
  ExampleS3OutpostsBucketPolicy:
    Type: 'AWS::S3Outposts::BucketPolicy'
    Properties:
      Bucket: !Ref ExampleS3OutpostsBucket
      PolicyDocument:
        Version: 2012-10-17
        ID: BucketPolicy
        Statement:
          - Sid: st1
            Effect: Allow
            Principal:
              AWS: 'arn:aws:iam::123456789012:root'
            Action: 's3-outposts:*'
            Resource: >-
              arn:aws:s3-outposts:us-east-1:123456789012:outpost/op-01ac5d28a6a232904/bucket/DOC-EXAMPLE-BUCKET
Outputs:
  ExampleS3OutpostsBucketARN:
    Description: The ARN of ExampleS3OutpostsBucket
    Value: !Ref ExampleS3OutpostsBucket
  ExampleS3OutpostsBucketPolicyARN:
    Description: The ARN of the BucketPolicy
    Value: !Ref ExampleS3OutpostsBucketPolicy
  ExampleS3OutpostsStackID:
    Description: The stack ID
    Value: !Ref 'AWS::StackID'
    Export:
      Name: !Sub '${AWS::StackName}-StackID'
```