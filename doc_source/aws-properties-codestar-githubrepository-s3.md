# AWS::CodeStar::GitHubRepository S3<a name="aws-properties-codestar-githubrepository-s3"></a>

The `S3` property type specifies information about the Amazon S3 bucket that contains the code to be committed to the new repository\.

 `S3` is a property of the `AWS::CodeStar::GitHubRepository` resource\.

## Syntax<a name="aws-properties-codestar-githubrepository-s3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codestar-githubrepository-s3-syntax.json"></a>

```
{
  "[Bucket](#cfn-codestar-githubrepository-s3-bucket)" : String,
  "[Key](#cfn-codestar-githubrepository-s3-key)" : String,
  "[ObjectVersion](#cfn-codestar-githubrepository-s3-objectversion)" : String
}
```

### YAML<a name="aws-properties-codestar-githubrepository-s3-syntax.yaml"></a>

```
  [Bucket](#cfn-codestar-githubrepository-s3-bucket): String
  [Key](#cfn-codestar-githubrepository-s3-key): String
  [ObjectVersion](#cfn-codestar-githubrepository-s3-objectversion): String
```

## Properties<a name="aws-properties-codestar-githubrepository-s3-properties"></a>

`Bucket`  <a name="cfn-codestar-githubrepository-s3-bucket"></a>
The name of the Amazon S3 bucket that contains the ZIP file with the content to be committed to the new repository\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Key`  <a name="cfn-codestar-githubrepository-s3-key"></a>
The S3 object key or file name for the ZIP file\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`ObjectVersion`  <a name="cfn-codestar-githubrepository-s3-objectversion"></a>
The object version of the ZIP file, if versioning is enabled for the Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.