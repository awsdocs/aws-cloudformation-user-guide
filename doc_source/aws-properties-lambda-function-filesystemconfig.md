# AWS::Lambda::Function FileSystemConfig<a name="aws-properties-lambda-function-filesystemconfig"></a>

Details about the connection between a Lambda function and an Amazon EFS file system\.

## Syntax<a name="aws-properties-lambda-function-filesystemconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-filesystemconfig-syntax.json"></a>

```
{
  "[Arn](#cfn-lambda-function-filesystemconfig-arn)" : String,
  "[LocalMountPath](#cfn-lambda-function-filesystemconfig-localmountpath)" : String
}
```

### YAML<a name="aws-properties-lambda-function-filesystemconfig-syntax.yaml"></a>

```
  [Arn](#cfn-lambda-function-filesystemconfig-arn): String
  [LocalMountPath](#cfn-lambda-function-filesystemconfig-localmountpath): String
```

## Properties<a name="aws-properties-lambda-function-filesystemconfig-properties"></a>

`Arn`  <a name="cfn-lambda-function-filesystemconfig-arn"></a>
The Amazon Resource Name \(ARN\) of the Amazon EFS access point that provides access to the file system\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `200`  
*Pattern*: `arn:aws[a-zA-Z-]*:elasticfilesystem:[a-z]{2}((-gov)|(-iso(b?)))?-[a-z]+-\d{1}:\d{12}:access-point/fsap-[a-f0-9]{17}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocalMountPath`  <a name="cfn-lambda-function-filesystemconfig-localmountpath"></a>
The path where the function can access the file system, starting with `/mnt/`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `160`  
*Pattern*: `^/mnt/[a-zA-Z0-9-_.]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)