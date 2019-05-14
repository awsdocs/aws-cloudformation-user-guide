# AWS::GameLift::Build<a name="aws-resource-gamelift-build"></a>

The `AWS::GameLift::Build` resource creates a build that includes all of the components to run your game server in an Amazon GameLift \(GameLift\) fleet\.

## Syntax<a name="aws-resource-gamelift-build-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-build-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Build",
  "Properties" : {
      "[Name](#cfn-gamelift-build-name)" : String,
      "[StorageLocation](#cfn-gamelift-build-storagelocation)" : [S3Location](aws-properties-gamelift-build-storagelocation.md),
      "[Version](#cfn-gamelift-build-version)" : String
    }
}
```

### YAML<a name="aws-resource-gamelift-build-syntax.yaml"></a>

```
Type: AWS::GameLift::Build
Properties : 
﻿  [Name](#cfn-gamelift-build-name) : String
﻿  [StorageLocation](#cfn-gamelift-build-storagelocation) : 
    [S3Location](aws-properties-gamelift-build-storagelocation.md)
﻿  [Version](#cfn-gamelift-build-version) : String
```

## Properties<a name="aws-resource-gamelift-build-properties"></a>

`Name`  <a name="cfn-gamelift-build-name"></a>
Descriptive label that is associated with a build\. Build names do not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageLocation`  <a name="cfn-gamelift-build-storagelocation"></a>
Information indicating where your game build files are stored\. Use this parameter only when creating a build with files stored in an Amazon S3 bucket that you own\. The storage location must specify an Amazon S3 bucket name and key, as well as a the ARN for a role that you set up to allow Amazon GameLift to access your Amazon S3 bucket\. The S3 bucket must be in the same region that you want to create a new build in\.  
*Required*: No  
*Type*: [S3Location](aws-properties-gamelift-build-storagelocation.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Version`  <a name="cfn-gamelift-build-version"></a>
Version that is associated with this build\. Version strings do not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-gamelift-build-return-values"></a>

### Ref<a name="aws-resource-gamelift-build-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the build ID, such as `mybuild-a01234b56-7890-1de2-f345-g67h8i901j2k`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-gamelift-build--examples"></a>

### Create GameLift build<a name="aws-resource-gamelift-build--examples--Create_GameLift_build"></a>

The following example creates a GameLift build named `MyGameServerBuild`\. The build package is located in an S3 bucket, specified by the `S3Bucket` and `S3Key` input parameters\. The example also creates the AWS Identity and Access Management \(IAM\) role that GameLift assumes so that it has permissions to download the build package files\.

#### JSON<a name="aws-resource-gamelift-build--examples--Create_GameLift_build--json"></a>

```
"BuildResource": {
  "Type": "AWS::GameLift::Build",
  "Properties": {
    "Name": "MyGameServerBuild",
    "Version": "v15",
    "StorageLocation": {
      "Bucket": "mybucket",
      "Key": "buildpackagefiles/",
      "RoleArn": { "Fn::GetAtt": [ "IAMRole", "Arn" ] }
    }
  }
},
"IAMRole": {
  "Type": "AWS::IAM::Role",
  "Properties": {
    "AssumeRolePolicyDocument": {
      "Version": "2012-10-17",
      "Statement": [
        {
          "Effect": "Allow",
          "Principal": { "Service": [ "gamelift.amazonaws.com" ] },
          "Action": [ "sts:AssumeRole" ]
        }
      ]
    },
    "Path": "/",
    "Policies": [
      {
        "PolicyName": "gamelift-s3-access-policy",
        "PolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Action": [ "s3:GetObject" ],
              "Resource": [ "arn:aws:s3:::mybucket/*" ]
            }
          ]
        }
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-gamelift-build--examples--Create_GameLift_build--yaml"></a>

```
BuildResource: 
  Type: AWS::GameLift::Build
  Properties: 
    Name: "MyGameServerBuild"
    Version: "v15"
    StorageLocation: 
      Bucket: "mybucket"
      Key: "buildpackagefiles/"
      RoleArn: 
        Fn::GetAtt: 
          - "IAMRole"
          - "Arn"
IAMRole: 
  Type: AWS::IAM::Role
  Properties: 
    AssumeRolePolicyDocument: 
      Version: "2012-10-17"
      Statement: 
        - 
          Effect: "Allow"
          Principal: 
            Service: 
              - "gamelift.amazonaws.com"
          Action: 
            - "sts:AssumeRole"
    Path: "/"
    Policies: 
      - 
        PolicyName: "gamelift-s3-access-policy"
        PolicyDocument: 
          Version: "2012-10-17"
          Statement: 
            - 
              Effect: "Allow"
              Action: 
                - "s3:GetObject"
              Resource: 
                - "arn:aws:s3:::mybucket/*"
```

## See Also<a name="aws-resource-gamelift-build--seealso"></a>
+  [CreateBuild](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateBuild.html) in the *Amazon GameLift API Reference* 