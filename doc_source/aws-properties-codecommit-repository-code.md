# AWS::CodeCommit::Repository Code<a name="aws-properties-codecommit-repository-code"></a>

Information about code to be committed\.

## Syntax<a name="aws-properties-codecommit-repository-code-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codecommit-repository-code-syntax.json"></a>

```
{
  "[BranchName](#cfn-codecommit-repository-code-branchname)" : String,
  "[S3](#cfn-codecommit-repository-code-s3)" : S3
}
```

### YAML<a name="aws-properties-codecommit-repository-code-syntax.yaml"></a>

```
  [BranchName](#cfn-codecommit-repository-code-branchname): String
  [S3](#cfn-codecommit-repository-code-s3): 
    S3
```

## Properties<a name="aws-properties-codecommit-repository-code-properties"></a>

`BranchName`  <a name="cfn-codecommit-repository-code-branchname"></a>
Optional\. Specifies a branch name to be used as the default branch when importing code into a repository\. If this property is not set, the name *master* will be used for the default branch for the repository\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3`  <a name="cfn-codecommit-repository-code-s3"></a>
Information about the Amazon S3 bucket that contains a ZIP file of code to be committed to the repository\.  
*Required*: Yes  
*Type*: [S3](aws-properties-codecommit-repository-s3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)