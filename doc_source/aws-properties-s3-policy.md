# AWS::S3::BucketPolicy<a name="aws-properties-s3-policy"></a>

Applies an Amazon S3 bucket policy to an Amazon S3 bucket\.

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
Properties : 
﻿  [Bucket](#aws-properties-s3-policy-bucket) : String
﻿  [PolicyDocument](#aws-properties-s3-policy-policydocument) : Json
```

## Properties<a name="aws-properties-s3-policy-properties"></a>

`Bucket`  <a name="aws-properties-s3-policy-bucket"></a>
The name of the Amazon S3 bucket to which the policy applies\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyDocument`  <a name="aws-properties-s3-policy-policydocument"></a>
 A policy document containing permissions to add to the specified bucket\. For more information, see [Access Policy Language Overview](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-policy-language-overview.html) in the *Amazon Simple Storage Service Developer Guide*\.   
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-policy--examples"></a>

### Bucket policy that allows GET requests from specific referers<a name="aws-properties-s3-policy--examples--Bucket_policy_that_allows_GET_requests_from_specific_referers"></a>

 The following sample is a bucket policy that is attached to the myExampleBucket bucket and allows GET requests that originate from www\.example\.com and example\.com: 

#### JSON<a name="aws-properties-s3-policy--examples--Bucket_policy_that_allows_GET_requests_from_specific_referers--json"></a>

```
"SampleBucketPolicy" : {
  "Type" : "AWS::S3::BucketPolicy",
  "Properties" : {
    "Bucket" : {"Ref" : "myExampleBucket"},
    "PolicyDocument": {
      "Statement":[{
	    "Action":["s3:GetObject"],
	    "Effect":"Allow",
	    "Resource": { "Fn::Join" : ["", ["arn:aws:s3:::", { "Ref" : "myExampleBucket" } , "/*" ]]},
	    "Principal":"*",
        "Condition":{
          "StringLike":{
            "aws:Referer":[
              "http://www.example.com/*",
              "http://example.com/*"
            ]
          }
        }
      }]
    }
  }
}
```

#### YAML<a name="aws-properties-s3-policy--examples--Bucket_policy_that_allows_GET_requests_from_specific_referers--yaml"></a>

```
SampleBucketPolicy: 
  Type: AWS::S3::BucketPolicy
  Properties: 
    Bucket: 
      Ref: "myExampleBucket"
    PolicyDocument: 
      Statement: 
        - 
          Action: 
            - "s3:GetObject"
          Effect: "Allow"
          Resource: 
            Fn::Join: 
              - ""
              - 
                - "arn:aws:s3:::"
                - 
                  Ref: "myExampleBucket"
                - "/*"
          Principal: "*"
          Condition: 
            StringLike: 
              aws:Referer: 
                - "http://www.example.com/*"
                - "http://example.com/*"
```