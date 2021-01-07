# AWS::GameLift::Build<a name="aws-resource-gamelift-build"></a>

The `AWS::GameLift::Build` resource creates a game server build that is installed and run on instances in an Amazon GameLift fleet\. This resource points to an Amazon S3 location that contains a zip file with all of the components of the game server build\.

## Syntax<a name="aws-resource-gamelift-build-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-build-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Build",
  "Properties" : {
      "[Name](#cfn-gamelift-build-name)" : String,
      "[OperatingSystem](#cfn-gamelift-build-operatingsystem)" : String,
      "[StorageLocation](#cfn-gamelift-build-storagelocation)" : S3Location,
      "[Version](#cfn-gamelift-build-version)" : String
    }
}
```

### YAML<a name="aws-resource-gamelift-build-syntax.yaml"></a>

```
Type: AWS::GameLift::Build
Properties: 
  [Name](#cfn-gamelift-build-name): String
  [OperatingSystem](#cfn-gamelift-build-operatingsystem): String
  [StorageLocation](#cfn-gamelift-build-storagelocation): 
    S3Location
  [Version](#cfn-gamelift-build-version): String
```

## Properties<a name="aws-resource-gamelift-build-properties"></a>

`Name`  <a name="cfn-gamelift-build-name"></a>
A descriptive label that is associated with a build\. Build names do not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OperatingSystem`  <a name="cfn-gamelift-build-operatingsystem"></a>
The operating system that the game server binaries are built to run on\. This value determines the type of fleet resources that you can use for this build\. If your game build contains multiple executables, they all must run on the same operating system\. If an operating system is not specified when creating a build, Amazon GameLift uses the default value \(WINDOWS\_2012\)\. This value cannot be changed later\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AMAZON_LINUX | AMAZON_LINUX_2 | WINDOWS_2012`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageLocation`  <a name="cfn-gamelift-build-storagelocation"></a>
Information indicating where your game build files are stored\. Use this parameter only when creating a build with files stored in an S3 bucket that you own\. The storage location must specify an S3 bucket name and key\. The location must also specify a role ARN that you set up to allow Amazon GameLift to access your S3 bucket\. The S3 bucket and your new build must be in the same Region\.  
*Required*: No  
*Type*: [S3Location](aws-properties-gamelift-build-storagelocation.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-gamelift-build-version"></a>
Version information that is associated with this build\. Version strings do not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-gamelift-build-return-values"></a>

### Ref<a name="aws-resource-gamelift-build-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the build ID, such as `build-1111aaaa-22bb-33cc-44dd-5555eeee66ff`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-gamelift-build--examples"></a>

### Create a Custom Game Server Build<a name="aws-resource-gamelift-build--examples--Create_a_Custom_Game_Server_Build"></a>

The following example creates a GameLift build named `MyGameServerBuild`\. The build package is located in an S3 bucket, specified by the `S3Bucket` and `S3Key` input parameters\. The example also creates the AWS Identity and Access Management \(IAM\) role that GameLift assumes so that it has permissions to download the build package files\.

#### JSON<a name="aws-resource-gamelift-build--examples--Create_a_Custom_Game_Server_Build--json"></a>

```
{
    "Resources": {
        "IAMRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "cloudformation.amazonaws.com",
                                    "gamelift.amazonaws.com"
                                ]
                            },
                            "Action": "sts:AssumeRole"
                        }
                    ]
                },
                "RoleName": "BuildIAMRole",
                "Policies": [
                    {
                        "PolicyName": "gamelift-s3-access-policy",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": [
                                        "s3:GetObject",
                                        "s3:GetObjectVersion",
                                        "s3:GetObjectMetadata",
                                        "s3:*Object*"
                                    ],
                                    "Resource": [
                                        "arn:aws:s3:::MyBucketName/*"
                                    ]
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "BuildResource": {
            "Type": "AWS::GameLift::Build",
            "Properties": {
                "Name": "MyGameServerBuild",
                "Version": "v1.0",
                "OperatingSystem": "WINDOWS_2012",
                "StorageLocation": {
                    "Bucket": "MyBucketName",
                    "Key": "MyGameBuildFiles.zip",
                    "RoleArn": {
                        "Fn::GetAtt": [
                            "IAMRole",
                            "Arn"
                        ]
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-build--examples--Create_a_Custom_Game_Server_Build--yaml"></a>

```
Resources:
  IAMRole:
    Type: "AWS::IAM::Role"
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: "Allow"
            Principal:
              Service: ["cloudformation.amazonaws.com", "gamelift.amazonaws.com"]
            Action: "sts:AssumeRole"
      RoleName: "BuildIAMRole"
      Policies:
        - PolicyName: gamelift-s3-access-policy
          PolicyDocument:
            Version: '2012-10-17'
            Statement:
              - Effect: Allow
                Action:
                  - "s3:GetObject"
                  - "s3:GetObjectVersion"
                  - "s3:GetObjectMetadata"
                  - "s3:*Object*"
                Resource:
                  - "arn:aws:s3:::MyBucketName/*"
  BuildResource:
    Type: AWS::GameLift::Build
    Properties:
      Name: MyGameServerBuild
      Version: v1.0
      OperatingSystem: WINDOWS_2012
      StorageLocation:
        Bucket: "MyBucketName"
        Key: "MyGameBuildFiles.zip"        
        RoleArn: !GetAtt IAMRole.Arn
```

## See also<a name="aws-resource-gamelift-build--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Create a Build with Files in Amazon S3](https://docs.aws.amazon.com/gamelift/latest/developerguide/gamelift-build-cli-uploading.html#gamelift-build-cli-uploading-create-build) in the *Amazon GameLift Developer Guide*
+ [ Upload Script Files in Amazon S3](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-script-uploading.html#realtime-script-uploading-s3) in the *Amazon GameLift Developer Guide*
+  [CreateBuild](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateBuild.html) in the *Amazon GameLift API Reference* 

