# AWS::Include transform<a name="create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform"></a>

Use the `AWS::Include` transform, which is a macro hosted by AWS CloudFormation, to insert boilerplate content into your templates\. The `AWS::Include` transform lets you create a reference to a template snippet in an Amazon S3 bucket\. When [Creating a change set](using-cfn-updating-stacks-changesets-create.md) or [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md), and the templates reference `AWS::Include`, AWS CloudFormation inserts the contents of the specified file at the location of the transform in the template\. The `AWS::Include` function behaves similarly to an `include`, `copy`, or `import` directive in programming languages\.

For example, you might have a Lambda function that you want to reuse in one or more AWS CloudFormation templates\. 

## Usage<a name="aws-include-transform-usage"></a>

You can use the `AWS::Include` transform anywhere within the AWS CloudFormation template except in the template parameters section or the template version field\. For example, you can use `AWS::Include` in the mappings section\. 

### Syntax at the top level of a template<a name="aws-include-syntax-top-level-overview"></a>

To include the `AWS::Include` transform at the top level of a template, in the `Transform` section, use the following syntax\.

#### JSON<a name="aws-include-syntax-top-level.json"></a>

```
1. {
2.    "Transform" : {
3.        "Name" : "AWS::Include",
4.        "Parameters" : {
5.            "Location" : "s3://MyAmazonS3BucketName/MyFileName.json"
6.         }
7.     }
8. }
```

#### YAML<a name="aws-include-syntax-top-level.yaml"></a>

```
1. Transform:
2.   Name: 'AWS::Include'
3.   Parameters:
4.     Location: 's3://MyAmazonS3BucketName/MyFileName.yaml'
```

### Syntax when the transform is embedded within a section of a template<a name="aws-include-syntax-embedded-within-section-overview"></a>

To include a transform that is embedded within a section, use the ``Fn::Transform`` intrinsic function and the following syntax\.

#### JSON<a name="aws-include-syntax-within-section.json"></a>

```
1. {
2.    "Fn::Transform" : {
3.        "Name" : "AWS::Include",
4.        "Parameters" : {
5.            "Location" : "s3://MyAmazonS3BucketName/MyFileName.json"
6.         }
7.     }
8. }
```

#### YAML<a name="aws-include-syntax-embedded-within-section.yaml"></a>

```
1. 'Fn::Transform':
2.   Name: 'AWS::Include'
3.   Parameters:
4.     Location: s3://MyAmazonS3BucketName/MyFileName.yaml
```

## Parameters<a name="aws-include-transform-parameters"></a>

*Location*

The location is an Amazon S3 URI, with a specific file name in an S3 bucket\. For example, `s3://MyBucketName/MyFile.yaml`\.

## Remarks<a name="aws-include-transform-remarks"></a>

When using `AWS::Include`, keep the following considerations in mind\. For general considerations about using macros, see [Considerations when creating AWS CloudFormation macro definitions](template-macros.md#template-macros-considerations)
+ We currently support Amazon S3 URI, but no other Amazon S3 format \(such as Amazon S3 ARN\)\. It must be an Amazon S3 bucket, as opposed to something like a GitHub repository\.
+ Anyone with access to the Amazon S3 URL can include the snippet in their template\.
+ Your template snippets must be valid YAML or JSON\.
+ Your template snippets must be valid key–value objects, for example `"KeyName": "keyValue"`\.
+ You can't use `AWS::Include` to reference a template snippet that also uses `AWS::Include`\.
+ If your snippets change, your stack doesn't automatically pick up those changes\. To get those changes, you must update the stack with the updated snippets\. If you update your stack, make sure your included snippets haven't changed without your knowledge\. To verify before updating the stack, check the change set\.
+ When creating templates and snippets, you can mix YAML and JSON template languages\.
+ We do not currently support using shorthand notations for YAML snippets\.
+ You can provide a cross\-region replication Amazon S3 URI with `AWS::Include`\. Make sure you check Amazon S3 bucket names when accessing cross\-region replication objects\. For more information, see [Cross\-Region replication](http://docs.aws.amazon.com/AmazonS3/latest/dev/crr.html)\.

## Example<a name="aws-include-transform-examples"></a>

The following example shows how to use the `AWS::Include` transform to execute a wait condition handle\.

Both the JSON and the YAML versions use the following wait condition snippet\. Save the file as `single_wait_condition.yaml`, and store it in an S3 bucket with the same name as *MyAmazonS3BucketName*\.

```
WebServerWaitHandle:
  Type: 'AWS::CloudFormation::WaitConditionHandle'
```

### JSON<a name="aws-include-example.json"></a>

```
 1. {
 2.    "Resources": {
 3.       "MyWaitHandle": {
 4.          "Type": "AWS::CloudFormation::WaitConditionHandle"
 5.       },
 6.       "Fn::Transform": {
 7.          "Name": "AWS::Include",
 8.          "Parameters": {
 9.             "Location": "s3://MyAmazonS3BucketName/single_wait_condition.yaml"
10.          }
11.       }
12.    }
13. }
```

### YAML<a name="aws-include-example.yaml"></a>

```
1. Resources:
2.   MyWaitHandle:
3.     Type: 'AWS::CloudFormation::WaitConditionHandle'
4.   'Fn::Transform':
5.     Name: 'AWS::Include'
6.     Parameters:
7.       Location : "s3://MyAmazonS3BucketName/single_wait_condition.yaml"
```