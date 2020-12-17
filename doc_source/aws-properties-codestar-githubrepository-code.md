# AWS::CodeStar::GitHubRepository Code<a name="aws-properties-codestar-githubrepository-code"></a>

The `Code` property type specifies information about code to be committed\.

 `Code` is a property of the `AWS::CodeStar::GitHubRepository` resource\.

## Syntax<a name="aws-properties-codestar-githubrepository-code-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codestar-githubrepository-code-syntax.json"></a>

```
{
  "[S3](#cfn-codestar-githubrepository-code-s3)" : S3
}
```

### YAML<a name="aws-properties-codestar-githubrepository-code-syntax.yaml"></a>

```
  [S3](#cfn-codestar-githubrepository-code-s3): 
    S3
```

## Properties<a name="aws-properties-codestar-githubrepository-code-properties"></a>

`S3`  <a name="cfn-codestar-githubrepository-code-s3"></a>
Information about the Amazon S3 bucket that contains a ZIP file of code to be committed to the repository\.   
*Required*: Yes  
*Type*: [S3](aws-properties-codestar-githubrepository-s3.md)  
*Update requires*: Updates are not supported\.