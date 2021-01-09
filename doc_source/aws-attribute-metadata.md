# Metadata attribute<a name="aws-attribute-metadata"></a>

The Metadata attribute enables you to associate structured data with a resource\. By adding a Metadata attribute to a resource, you can add data in JSON or YAML to the resource declaration\. In addition, you can use intrinsic functions \(such as [GetAtt](intrinsic-function-reference-getatt.md) and [Ref](intrinsic-function-reference-ref.md)\), parameters, and pseudo parameters within the Metadata attribute to add those interpreted values\.

**Note**  
AWS CloudFormation does not validate the syntax within the Metadata attribute\.

**Important**  
CloudFormation does not redact or obfuscate any information you include in the Metadata attribute\. We strongly recommend you do not use this section to store sensitive information, such as passwords or secrets\.

You can retrieve this data using the AWS command [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-resource.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-resource.html) or the [DescribeStackResource action](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeStackResource.html)\.

## Example<a name="w7739ab1c33c23c19c11"></a>

The following template contains an Amazon S3 bucket resource with a Metadata attribute\.

### JSON<a name="aws-attribute-metadata-example.json"></a>

```
 1. {
 2.    "AWSTemplateFormatVersion" : "2010-09-09",
 3.    "Resources" : {
 4.       "MyS3Bucket" : {
 5.          "Type" : "AWS::S3::Bucket",
 6.          "Metadata" : { 
 7.             "Object1" : "Location1",  
 8.             "Object2" : "Location2" 
 9.          }
10.       }
11.    }
12. }
```

### YAML<a name="aws-attribute-metadata-example.yaml"></a>

```
1. AWSTemplateFormatVersion: '2010-09-09'
2. Resources:
3.   MyS3Bucket:
4.     Type: AWS::S3::Bucket
5.     Metadata:
6.       Object1: Location1
7.       Object2: Location2
```