# AWS::Include Transform<a name="create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform"></a>

You can use the `AWS::Include` transform to work with template snippets that are stored separately from the main AWS CloudFormation template\. When you specify `Name: 'AWS::Include'` and the `Location` parameter, the `Transform` key is a placeholder where snippets are injected\. AWS CloudFormation inserts those snippets into your main template when [Creating a Change Set](using-cfn-updating-stacks-changesets-create.md) or [Updating Stacks Using Change Sets](using-cfn-updating-stacks-changesets.md)\.

You might have a Lambda function that you want to reuse in one or more AWS CloudFormation templates\. The `AWS::Include` transform lets you create a reference to a transform snippet in an Amazon S3 bucket\. You can add `AWS::Include` to the `Transform` function in your AWS CloudFormation template\. The `AWS::Include` function behaves similarly to an `include`, `copy`, or `import` directive in programming languages\.

## Usage<a name="aws-include-transform-usage"></a>

You can use the `AWS::Include` transform anywhere within the AWS CloudFormation template except in the template parameters section or the template version field\. For example, you can use `AWS::Include` in the mappings section\. 

### Syntax at the Top Level of a Template<a name="aws-include-syntax-top-level-overview"></a>

To include a transform at the top level of a template, use the following syntax\.

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

### Syntax When the Transform Is Embedded Within a Section of a Template<a name="aws-include-syntax-embedded-within-section-overview"></a>

To include a transform that is embedded within a section, use the following syntax\.

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

When using `AWS::Include`, keep the following in mind:
+ `AWS::Include` is supported only in regions where AWS Lambda is available\. For a list of regions where Lambda is available, see [http://docs.aws.amazon.com/general/latest/gr/rande.html#lambda_region](http://docs.aws.amazon.com/general/latest/gr/rande.html#lambda_region)\.
+ We currently support Amazon S3 URI, but no other Amazon S3 format \(such as Amazon S3 ARN\)\. It must be an Amazon S3 bucket, as opposed to something like a GitHub repository\.
+ Anyone with access to the Amazon S3 URL can include the snippet in their template\.
+ Your template snippets must be valid YAML or JSON\.
+ Your template snippets must be valid key–value objects, for example `"KeyName": "keyValue"`\.
+ A template snippet must pass validation checks for a create stack or update stack operation\.
+ AWS CloudFormation resolves transforms first, and then processes the template\. The resulting template must be valid JSON or YAML and must not exceed the template size limit\.
+ If your snippets change, your stack doesn't automatically pick up those changes\. To get those changes, you must update the stack with the updated snippets\. If you update your stack, make sure your included snippets haven't changed without your knowledge\. To verify before updating the stack, check the change set\.
+ When using the update rollback feature, AWS CloudFormation uses a copy of the original template\. It will roll back to the original template even if the included snippet was changed\.
+ Nested transforms do not work because we do not process transforms iteratively\.
+ When creating templates and snippets, you can mix YAML and JSON template languages\.
+ We do not currently support using shorthand notations for YAML snippets\.
+ The `Fn::ImportValue` intrinsic function isn't currently supported in transforms\.
+ You can use multiple transforms within a single template\. Nevertheless, you cannot simultaneously have `AWS::Include` transforms at both the top level of a template and embedded within a section of a template\.
+ You can provide a cross\-region replication Amazon S3 URI with `AWS::Include`\. Be sure to check Amazon S3 bucket names when accessing cross\-region replication objects\. For more information, see [Cross\-Region Replication](http://docs.aws.amazon.com/AmazonS3/latest/dev/crr.html)\.

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