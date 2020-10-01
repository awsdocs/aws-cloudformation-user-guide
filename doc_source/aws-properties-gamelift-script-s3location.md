# AWS::GameLift::Script S3Location<a name="aws-properties-gamelift-script-s3location"></a>

The location in Amazon S3 where build or script files can be stored for access by Amazon GameLift\. 

## Syntax<a name="aws-properties-gamelift-script-s3location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-script-s3location-syntax.json"></a>

```
{
  "[Bucket](#cfn-gamelift-script-s3location-bucket)" : String,
  "[Key](#cfn-gamelift-script-s3location-key)" : String,
  "[ObjectVersion](#cfn-gamelift-script-s3location-objectversion)" : String,
  "[RoleArn](#cfn-gamelift-script-s3location-rolearn)" : String
}
```

### YAML<a name="aws-properties-gamelift-script-s3location-syntax.yaml"></a>

```
  [Bucket](#cfn-gamelift-script-s3location-bucket): String
  [Key](#cfn-gamelift-script-s3location-key): String
  [ObjectVersion](#cfn-gamelift-script-s3location-objectversion): String
  [RoleArn](#cfn-gamelift-script-s3location-rolearn): String
```

## Properties<a name="aws-properties-gamelift-script-s3location-properties"></a>

`Bucket`  <a name="cfn-gamelift-script-s3location-bucket"></a>
An S3 bucket identifier\. This is the name of the S3 bucket\.  
GameLift currently does not support uploading from S3 buckets with names that contain a dot \(\.\)\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-gamelift-script-s3location-key"></a>
The name of the zip file that contains the build files or script files\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectVersion`  <a name="cfn-gamelift-script-s3location-objectversion"></a>
The version of the file, if object versioning is turned on for the bucket\. Amazon GameLift uses this information when retrieving files from an S3 bucket that you own\. Use this parameter to specify a specific version of the file\. If not set, the latest version of the file is retrieved\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-gamelift-script-s3location-rolearn"></a>
The Amazon Resource Name \([ARN](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-arn-format.html)\) for an IAM role that allows Amazon GameLift to access the S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)