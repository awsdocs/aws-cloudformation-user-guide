# AWS::Synthetics::Canary Code<a name="aws-properties-synthetics-canary-code"></a>

Use this structure to input your script code for the canary\. This structure contains the Lambda handler with the location where the canary should start running the script\. If the script is stored in an S3 bucket, the bucket name, key, and version are also included\. If the script is passed into the canary directly, the script code is contained in the value of `Script`\. 

## Syntax<a name="aws-properties-synthetics-canary-code-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-code-syntax.json"></a>

```
{
  "[Handler](#cfn-synthetics-canary-code-handler)" : String,
  "[S3Bucket](#cfn-synthetics-canary-code-s3bucket)" : String,
  "[S3Key](#cfn-synthetics-canary-code-s3key)" : String,
  "[S3ObjectVersion](#cfn-synthetics-canary-code-s3objectversion)" : String,
  "[Script](#cfn-synthetics-canary-code-script)" : String
}
```

### YAML<a name="aws-properties-synthetics-canary-code-syntax.yaml"></a>

```
  [Handler](#cfn-synthetics-canary-code-handler): String
  [S3Bucket](#cfn-synthetics-canary-code-s3bucket): String
  [S3Key](#cfn-synthetics-canary-code-s3key): String
  [S3ObjectVersion](#cfn-synthetics-canary-code-s3objectversion): String
  [Script](#cfn-synthetics-canary-code-script): String
```

## Properties<a name="aws-properties-synthetics-canary-code-properties"></a>

`Handler`  <a name="cfn-synthetics-canary-code-handler"></a>
The entry point to use for the source code when running the canary\. This value must end with the string `.handler`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Bucket`  <a name="cfn-synthetics-canary-code-s3bucket"></a>
If your canary script is located in S3, specify the bucket name here\. The bucket must already exist\.   
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Key`  <a name="cfn-synthetics-canary-code-s3key"></a>
The S3 key of your script\. For more information, see [Working with Amazon S3 Objects](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingObjects.html)\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3ObjectVersion`  <a name="cfn-synthetics-canary-code-s3objectversion"></a>
The S3 version ID of your script\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Script`  <a name="cfn-synthetics-canary-code-script"></a>
If you input your canary script directly into the canary instead of referring to an S3 location, the value of this parameter is the script in plain text\. It can be up to 5 MB\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)