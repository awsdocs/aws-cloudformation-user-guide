# AWS::GameLift::Build S3Location<a name="aws-properties-gamelift-build-storagelocation"></a>

Location in Amazon Simple Storage Service \(Amazon S3\) where build files can be stored for access by Amazon GameLift\. For more details, see the [Uploading a Build to Amazon GameLift](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-build-cli-uploading.html) in the *Amazon GameLift Developer Guide*\.

## Syntax<a name="aws-properties-gamelift-build-storagelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-build-storagelocation-syntax.json"></a>

```
{
  "[Bucket](#cfn-gamelift-build-storage-bucket)" : String,
  "[Key](#cfn-gamelift-build-storage-key)" : String,
  "[RoleArn](#cfn-gamelift-build-storage-rolearn)" : String
}
```

### YAML<a name="aws-properties-gamelift-build-storagelocation-syntax.yaml"></a>

```
﻿  [Bucket](#cfn-gamelift-build-storage-bucket) : String
﻿  [Key](#cfn-gamelift-build-storage-key) : String
﻿  [RoleArn](#cfn-gamelift-build-storage-rolearn) : String
```

## Properties<a name="aws-properties-gamelift-build-storagelocation-properties"></a>

`Bucket`  <a name="cfn-gamelift-build-storage-bucket"></a>
Amazon S3 bucket identifier\. This is the name of the S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Key`  <a name="cfn-gamelift-build-storage-key"></a>
Name of the zip file containing the build files or script files\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-gamelift-build-storage-rolearn"></a>
Amazon Resource Name \([ARN](https://docs.aws.amazon.com/AmazonS3/latest/dev/s3-arn-format.html)\) for an IAM role that allows Amazon GameLift to access the S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See Also<a name="aws-properties-gamelift-build-storagelocation--seealso"></a>
+  [S3Location](https://docs.aws.amazon.com/gamelift/latest/apireference/API_S3Location.html) in the *Amazon GameLift API Reference* 