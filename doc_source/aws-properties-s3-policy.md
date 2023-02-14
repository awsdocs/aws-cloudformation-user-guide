# AWS::S3::BucketPolicy<a name="aws-properties-s3-policy"></a>

Applies an Amazon S3 bucket policy to an Amazon S3 bucket\. If you are using an identity other than the root user of the AWS account that owns the bucket, the calling identity must have the `PutBucketPolicy` permissions on the specified bucket and belong to the bucket owner's account in order to use this operation\.

If you don't have `PutBucketPolicy` permissions, Amazon S3 returns a `403 Access Denied` error\. If you have the correct permissions, but you're not using an identity that belongs to the bucket owner's account, Amazon S3 returns a `405 Method Not Allowed` error\.

**Important**  
 As a security precaution, the root user of the AWS account that owns a bucket can always use this operation, even if the policy explicitly denies the root user the ability to perform this action\. 

For more information, see [Bucket policy examples](https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html)\.

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
 A policy document containing permissions to add to the specified bucket\. In IAM, you must provide policy documents in JSON format\. However, in CloudFormation you can provide the policy in JSON or YAML format because CloudFormation converts YAML to JSON before submitting it to IAM\. For more information, see the AWS::IAM::Policy [PolicyDocument](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-policy.html#cfn-iam-policy-policydocument) resource description in this guide and [Access Policy Language Overview](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-policy-language-overview.html) in the *Amazon S3 User Guide*\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-policy--examples"></a>



### Bucket policy that allows GET requests from specific referers<a name="aws-properties-s3-policy--examples--Bucket_policy_that_allows_GET_requests_from_specific_referers"></a>

The following sample is a bucket policy that is attached to the DOC\-EXAMPLE\-BUCKET bucket and allows GET requests that originate from www\.example\.com and example\.net: 

**Important**  
This key should be used carefully\. It is dangerous to include a publicly known referer header value\. Unauthorized parties can use modified or custom browsers to provide any `aws:referer` value that they choose\. As a result, `aws:referer` should not be used to prevent unauthorized parties from making direct AWS requests\. It is offered only to allow customers to protect their digital content, such as content stored in Amazon S3, from being referenced on unauthorized third\-party sites\. For more information, see [https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-referer](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-referer) in the *IAM User Guide*\.

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
                "Version": "2012-10-17",
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
  Type: AWS::S3::BucketPolicy
  Properties:
    Bucket: !Ref DOC-EXAMPLE-BUCKET
    PolicyDocument:
      Version: 2012-10-17
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