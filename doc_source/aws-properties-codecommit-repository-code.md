# AWS::CodeCommit::Repository Code<a name="aws-properties-codecommit-repository-code"></a>

Information about code to be committed\.

## Syntax<a name="aws-properties-codecommit-repository-code-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codecommit-repository-code-syntax.json"></a>

```
{
  "[S3](#cfn-codecommit-repository-code-s3)" : [S3](aws-properties-codecommit-repository-s3.md)
}
```

### YAML<a name="aws-properties-codecommit-repository-code-syntax.yaml"></a>

```
  [S3](#cfn-codecommit-repository-code-s3): 
    [S3](aws-properties-codecommit-repository-s3.md)
```

## Properties<a name="aws-properties-codecommit-repository-code-properties"></a>

`S3`  <a name="cfn-codecommit-repository-code-s3"></a>
Information about the Amazon S3 bucket that contains a ZIP file of code to be committed to the repository\.  
*Required*: Yes  
*Type*: [S3](aws-properties-codecommit-repository-s3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)