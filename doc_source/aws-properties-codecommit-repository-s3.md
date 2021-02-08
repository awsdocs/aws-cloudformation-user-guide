# AWS::CodeCommit::Repository S3<a name="aws-properties-codecommit-repository-s3"></a>

Information about the Amazon S3 bucket that contains the code that will be committed to the new repository\.

## Syntax<a name="aws-properties-codecommit-repository-s3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codecommit-repository-s3-syntax.json"></a>

```
{
  "[Bucket](#cfn-codecommit-repository-s3-bucket)" : String,
  "[Key](#cfn-codecommit-repository-s3-key)" : String,
  "[ObjectVersion](#cfn-codecommit-repository-s3-objectversion)" : String
}
```

### YAML<a name="aws-properties-codecommit-repository-s3-syntax.yaml"></a>

```
  [Bucket](#cfn-codecommit-repository-s3-bucket): String
  [Key](#cfn-codecommit-repository-s3-key): String
  [ObjectVersion](#cfn-codecommit-repository-s3-objectversion): String
```

## Properties<a name="aws-properties-codecommit-repository-s3-properties"></a>

`Bucket`  <a name="cfn-codecommit-repository-s3-bucket"></a>
The name of the Amazon S3 bucket that contains the ZIP file with the content that will be committed to the new repository\. This can be specified using an ARN or the name of the bucket in the AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-codecommit-repository-s3-key"></a>
The key to use for accessing the Amazon S3 bucket\. This is an Amazon S3 object key as defined [in the Amazon S3 Developer Guide](https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html#BasicsKeys)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectVersion`  <a name="cfn-codecommit-repository-s3-objectversion"></a>
The object version of the ZIP file, if versioning is enabled for the Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)