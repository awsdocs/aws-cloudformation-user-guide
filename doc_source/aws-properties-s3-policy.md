# AWS::S3::BucketPolicy<a name="aws-properties-s3-policy"></a>

The AWS::S3::BucketPolicy type applies an Amazon S3 bucket policy to an Amazon S3 bucket\.

AWS::S3::BucketPolicy Snippet: [Declaring an Amazon S3 Bucket Policy](quickref-iam.md#scenario-bucket-policy)

**Topics**
+ [Syntax](#aws-resource-s3-bucketpolicy-syntax)
+ [Properties](#w3ab2c21c10e1036c11)
+ [Examples](#w3ab2c21c10e1036c13)

## Syntax<a name="aws-resource-s3-bucketpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3-bucketpolicy-syntax.json"></a>

```
{
   "Type" : "AWS::S3::BucketPolicy",
   "Properties" : {
      "[Bucket](#cfn-s3-bucketpolicy-bucket)" : String,
      "[PolicyDocument](#cfn-s3-bucketpolicy-policydocument)" : JSON
   }
}
```

### YAML<a name="aws-resource-s3-bucketpolicy-syntax.yaml"></a>

```
Type: "AWS::S3::BucketPolicy"
Properties: 
  [Bucket](#cfn-s3-bucketpolicy-bucket): String
  [PolicyDocument](#cfn-s3-bucketpolicy-policydocument): JSON
```

## Properties<a name="w3ab2c21c10e1036c11"></a>

`Bucket`  <a name="cfn-s3-bucketpolicy-bucket"></a>
The Amazon S3 bucket that the policy applies to\.  
*Required*: Yes  
*Type*: String  
You cannot update this property\. If you want to add or remove a bucket from a bucket policy, you must modify your AWS CloudFormation template by creating a new bucket policy resource and removing the old one\. Then use the modified template to update your AWS CloudFormation stack\.

`PolicyDocument`  <a name="cfn-s3-bucketpolicy-policydocument"></a>
A policy document containing permissions to add to the specified bucket\. For more information, see [Access Policy Language Overview](http://docs.aws.amazon.com/AmazonS3/latest/dev/access-policy-language-overview.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Examples<a name="w3ab2c21c10e1036c13"></a>

### Bucket policy that allows GET requests from specific referers<a name="w3ab2c21c10e1036c13b2"></a>

The following sample is a bucket policy that is attached to the `myExampleBucket` bucket and allows GET requests that originate from `www.example.com` and `example.com`:

#### JSON<a name="aws-resource-s3-bucketpolicy-example.json"></a>

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

#### YAML<a name="aws-resource-s3-bucketpolicy-example.yaml"></a>

```
SampleBucketPolicy: 
  Type: "AWS::S3::BucketPolicy"
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