# AWS::S3::BucketPolicy<a name="aws-properties-s3-policy"></a>

Applies an Amazon S3 bucket policy to an Amazon S3 bucket\. If you are using an identity other than the root user of the AWS account that owns the bucket, the calling identity must have the `PutBucketPolicy` permissions on the specified bucket and belong to the bucket owner's account in order to use this operation\.

If you don't have `PutBucketPolicy` permissions, Amazon S3 returns a `403 Access Denied` error\. If you have the correct permissions, but you're not using an identity that belongs to the bucket owner's account, Amazon S3 returns a `405 Method Not Allowed` error\.

**Important**  
 As a security precaution, the root user of the AWS account that owns a bucket can always use this operation, even if the policy explicitly denies the root user the ability to perform this action\. 

For more information about bucket policies, see [Using Bucket Policies and User Policies](https://docs.aws.amazon.com/AmazonS3/latest/dev/using-iam-policies.html)\.

The following operations are related to `PutBucketPolicy`:
+  [CreateBucket](https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html) 
+  [DeleteBucket](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html) 

## Syntax<a name="aws-properties-s3-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-policy-syntax.json"></a>

```
{
  "Type" : "AWS::S3::BucketPolicy",
  "Properties" : {
      "[Bucket](#aws-properties-s3-policy-bucket)" : String,
      "[PolicyDocument](#aws-properties-s3-policy-policydocument)" : Json
    }
}
```

### YAML<a name="aws-properties-s3-policy-syntax.yaml"></a>

```
Type: AWS::S3::BucketPolicy
Properties: 
  [Bucket](#aws-properties-s3-policy-bucket): String
  [PolicyDocument](#aws-properties-s3-policy-policydocument): Json
```

## Properties<a name="aws-properties-s3-policy-properties"></a>

`Bucket`  <a name="aws-properties-s3-policy-bucket"></a>
The name of the Amazon S3 bucket to which the policy applies\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyDocument`  <a name="aws-properties-s3-policy-policydocument"></a>
 A policy document containing permissions to add to the specified bucket\. In IAM, you must provide policy documents in JSON format\. However, in CloudFormation you can provide the policy in JSON or YAML format because CloudFormation converts YAML to JSON before submitting it to IAM\. For more information, see the AWS::IAM::Policy [PolicyDocument](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-policy.html#cfn-iam-policy-policydocument) resource description in this guide and [Access Policy Language Overview](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-policy-language-overview.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-policy--examples"></a>



### Bucket policy that allows GET requests from specific referers<a name="aws-properties-s3-policy--examples--Bucket_policy_that_allows_GET_requests_from_specific_referers"></a>

 The following sample is a bucket policy that is attached to the DOC\-EXAMPLE\-BUCKET bucket and allows GET requests that originate from www\.example\.com and example\.net: 

#### JSON<a name="aws-properties-s3-policy--examples--Bucket_policy_that_allows_GET_requests_from_specific_referers--json"></a>

```
{
    "SampleBucketPolicy": {
        "Type": "AWS::S3::BucketPolicy",
        "Properties": {
            "Bucket": {
                "Ref": "DOC-EXAMPLE-BUCKET"
            },
            "PolicyDocument": {
                "Statement": [
                    {
                        "Action": [
                            "s3:GetObject"
                        ],
                        "Effect": "Allow",
                        "Resource": {
                            "Fn::Join": [
                                "",
                                [
                                    "arn:aws:s3:::",
                                    {
                                        "Ref": "DOC-EXAMPLE-BUCKET"
                                    },
                                    "/*"
                                ]
                            ]
                        },
                        "Principal": "*",
                        "Condition": {
                            "StringLike": {
                                "aws:Referer": [
                                    "http://www.example.com/*",
                                    "http://example.net/*"
                                ]
                            }
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-policy--examples--Bucket_policy_that_allows_GET_requests_from_specific_referers--yaml"></a>

```
SampleBucketPolicy:
  Type: 'AWS::S3::BucketPolicy'
  Properties:
    Bucket: !Ref DOC-EXAMPLE-BUCKET
    PolicyDocument:
      Statement:
        - Action:
            - 's3:GetObject'
          Effect: Allow
          Resource: !Join
            - ''
            - - 'arn:aws:s3:::'
              - !Ref DOC-EXAMPLE-BUCKET
              - /*
          Principal: '*'
          Condition:
            StringLike:
              'aws:Referer':
                - 'http://www.example.com/*'
                - 'http://example.net/*'
```