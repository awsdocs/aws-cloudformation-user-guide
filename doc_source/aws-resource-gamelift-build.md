# AWS::GameLift::Build<a name="aws-resource-gamelift-build"></a>

The `AWS::GameLift::Build` resource creates a build that includes all of the components to run your game server in an Amazon GameLift \(GameLift\) fleet\.

**Topics**
+ [Syntax](#aws-resource-gamelift-build-syntax)
+ [Properties](#w3ab2c21c10d690b9)
+ [Return Value](#w3ab2c21c10d690c11)
+ [Example](#w3ab2c21c10d690c13)

## Syntax<a name="aws-resource-gamelift-build-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-build-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Build",
  "Properties" : {
    "[Name](#cfn-gamelift-build-name)" : String,
    "[StorageLocation](#cfn-gamelift-build-storagelocation)" : [StorageLocation](aws-properties-gamelift-build-storagelocation.md),
    "[Version](#cfn-gamelift-build-version)" : String
  }
}
```

### YAML<a name="aws-resource-gamelift-build-syntax.yaml"></a>

```
Type: "AWS::GameLift::Build"
Properties: 
  [Name](#cfn-gamelift-build-name): String
  [StorageLocation](#cfn-gamelift-build-storagelocation):
    [StorageLocation](aws-properties-gamelift-build-storagelocation.md)
  [Version](#cfn-gamelift-build-version): String
```

## Properties<a name="w3ab2c21c10d690b9"></a>

`Name`  <a name="cfn-gamelift-build-name"></a>
An identifier to associate with this build\. Build names don't need to be unique\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StorageLocation`  <a name="cfn-gamelift-build-storagelocation"></a>
The Amazon Simple Storage Service \(Amazon S3\) location where your build package files are located\.  
*Required*: No, but we recommend that you specify a location\. If you don't specify this property, you must manually upload your build package files to GameLift\.  
*Type*: [Amazon GameLift Build StorageLocation](aws-properties-gamelift-build-storagelocation.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Version`  <a name="cfn-gamelift-build-version"></a>
A version to associate with this build\. Version is useful if you want to track updates to your build package files\. Versions don't need to be unique\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d690c11"></a>

### Ref<a name="w3ab2c21c10d690c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the build ID, such as `mybuild-a01234b56-7890-1de2-f345-g67h8i901j2k`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d690c13"></a>

The following example creates a GameLift build named `MyGameServerBuild`\. The build package is located in an S3 bucket, specified by the `S3Bucket` and `S3Key` input parameters\. The example also creates the AWS Identity and Access Management \(IAM\) role that GameLift assumes so that it has permissions to download the build package files\.

### JSON<a name="aws-resource-gamelift-build-example.json"></a>

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

### YAML<a name="aws-resource-gamelift-build-example.yaml"></a>

```
BuildResource: 
  Type: "AWS::GameLift::Build"
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
  Type: "AWS::IAM::Role"
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