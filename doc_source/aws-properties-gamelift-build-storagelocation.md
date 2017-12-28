# Amazon GameLift Build StorageLocation<a name="aws-properties-gamelift-build-storagelocation"></a>

`StorageLocation` is a property of the [AWS::GameLift::Build](aws-resource-gamelift-build.md) resource that specifies the location of an Amazon GameLift \(GameLift\) build package files, such as the game server binaries\. For more information, see [Uploading a Build to Amazon GameLift](http://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-build-intro.html) in the *Amazon GameLift Developer Guide*\.

## Syntax<a name="w3ab2c21c14e1022b5"></a>

### JSON<a name="aws-properties-gamelift-build-storagelocation-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-gamelift-build-storage-bucket)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-gamelift-build-storage-key)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-gamelift-build-storage-rolearn)" : String
}
```

### YAML<a name="aws-properties-gamelift-build-storagelocation-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-gamelift-build-storage-bucket): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-gamelift-build-storage-key): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-gamelift-build-storage-rolearn): String
```

## Properties<a name="w3ab2c21c14e1022b7"></a>

`Bucket`  
The S3 bucket where the GameLift build package files are stored\.  
*Required: *Yes  
*Type*: String

`Key`  
The prefix \(folder name\) where the GameLift build package files are located\.  
*Required: *Yes  
*Type*: String

`RoleArn`  
An AWS Identity and Access Management \(IAM\) role Amazon Resource Name \(ARN\) that GameLift can assume to retrieve the build package files from Amazon Simple Storage Service \(Amazon S3\)\.  
*Required: *Yes  
*Type*: String