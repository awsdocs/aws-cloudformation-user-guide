# AWS::GameLift::Build S3Location<a name="aws-properties-gamelift-build-storagelocation"></a>

The location in Amazon S3 where build or script files are stored for access by Amazon GameLift\. 

## Syntax<a name="aws-properties-gamelift-build-storagelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-build-storagelocation-syntax.json"></a>

```
{
  "[Bucket](#cfn-gamelift-build-storage-bucket)" : String,
  "[Key](#cfn-gamelift-build-storage-key)" : String,
  "[ObjectVersion](#cfn-gamelift-build-object-verison)" : String,
  "[RoleArn](#cfn-gamelift-build-storage-rolearn)" : String
}
```

### YAML<a name="aws-properties-gamelift-build-storagelocation-syntax.yaml"></a>

```
  [Bucket](#cfn-gamelift-build-storage-bucket): String
  [Key](#cfn-gamelift-build-storage-key): String
  [ObjectVersion](#cfn-gamelift-build-object-verison): String
  [RoleArn](#cfn-gamelift-build-storage-rolearn): String
```

## Properties<a name="aws-properties-gamelift-build-storagelocation-properties"></a>

`Bucket`  <a name="cfn-gamelift-build-storage-bucket"></a>
An S3 bucket identifier\. This is the name of the S3 bucket\.  
GameLift currently does not support uploading from S3 buckets with names that contain a dot \(\.\)\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Key`  <a name="cfn-gamelift-build-storage-key"></a>
The name of the zip file that contains the build files or script files\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ObjectVersion`  <a name="cfn-gamelift-build-object-verison"></a>
The version of the file, if object versioning is turned on for the bucket\. Amazon GameLift uses this information when retrieving files from your S3 bucket\. To retrieve a specific version of the file, provide an object version\. To retrieve the latest version of the file, do not set this parameter\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-gamelift-build-storage-rolearn"></a>
The Amazon Resource Name \([ARN](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-arn-format.html)\) for an IAM role that allows Amazon GameLift to access the S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-gamelift-build-storagelocation--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Create a Build with Files in Amazon S3](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-build-cli-uploading.html#gamelift-build-cli-uploading-create-build) in the *Amazon GameLift Developer Guide*
+ [ Upload Script Files in Amazon S3](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-script-uploading.html#realtime-script-uploading-s3) in the *Amazon GameLift Developer Guide*
+  [S3Location](https://docs.aws.amazon.com/gamelift/latest/apireference/API_S3Location.html) in the *Amazon GameLift API Reference* 

