# AWS::GameLift::Script<a name="aws-resource-gamelift-script"></a>

The `AWS::GameLift::Script` resource creates a new script record for your Realtime Servers script\. Realtime scripts are JavaScript that provide configuration settings and optional custom game logic for your game\. The script is deployed when you create a Realtime Servers fleet to host your game sessions\. Script logic is executed during an active game session\. 

## Syntax<a name="aws-resource-gamelift-script-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-script-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Script",
  "Properties" : {
      "[Name](#cfn-gamelift-script-name)" : String,
      "[StorageLocation](#cfn-gamelift-script-storagelocation)" : S3Location,
      "[Version](#cfn-gamelift-script-version)" : String
    }
}
```

### YAML<a name="aws-resource-gamelift-script-syntax.yaml"></a>

```
Type: AWS::GameLift::Script
Properties: 
  [Name](#cfn-gamelift-script-name): String
  [StorageLocation](#cfn-gamelift-script-storagelocation): 
    S3Location
  [Version](#cfn-gamelift-script-version): String
```

## Properties<a name="aws-resource-gamelift-script-properties"></a>

`Name`  <a name="cfn-gamelift-script-name"></a>
A descriptive label that is associated with a script\. Script names do not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageLocation`  <a name="cfn-gamelift-script-storagelocation"></a>
The location in Amazon S3 where build or script files are stored for access by Amazon GameLift\.  
*Required*: Yes  
*Type*: [S3Location](aws-properties-gamelift-script-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-gamelift-script-version"></a>
The version that is associated with a build or script\. Version strings do not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-gamelift-script-return-values"></a>

### Ref<a name="aws-resource-gamelift-script-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ScriptId`, such as `script-1111aaaa-22bb-33cc-44dd-5555eeee66ff`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-gamelift-script-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-gamelift-script-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The unique Amazon Resource Name \(ARN\) for the script\.

`Id`  <a name="Id-fn::getatt"></a>
A unique identifier for a Realtime script\.

## Examples<a name="aws-resource-gamelift-script--examples"></a>

### Create a Realtime Servers Script<a name="aws-resource-gamelift-script--examples--Create_a_Realtime_Servers_Script"></a>

The following example creates a GameLift script named `MyRealtimeScript`\. The zipped script files are located in an S3 bucket, specified by the `S3Bucket` and `S3Key` input parameters\. The example also creates the AWS Identity and Access Management \(IAM\) role that GameLift assumes so that it has permissions to download the script files\.

#### JSON<a name="aws-resource-gamelift-script--examples--Create_a_Realtime_Servers_Script--json"></a>

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
                "RoleName": "ScriptIAMRole",
                "Policies": [
                    {
                        "PolicyName": "ScriptResourceIAMPolicy",
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
                                        "*"
                                    ]
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "ScriptResource": {
            "Type": "AWS::GameLift::Script",
            "Properties": {
                "Name": "MyRealtimeScript",
                "Version": "v1.0",
                "StorageLocation": {
                    "Bucket": "MyBucketName",
                    "Key": "MyScriptFiles.zip",
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

#### YAML<a name="aws-resource-gamelift-script--examples--Create_a_Realtime_Servers_Script--yaml"></a>

```
Resources:
  IAMRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: "Allow"
            Principal:
              Service: ["cloudformation.amazonaws.com", "gamelift.amazonaws.com"]
            Action: "sts:AssumeRole"
      RoleName: "ScriptIAMRole"
      Policies:
        - PolicyName: ScriptResourceIAMPolicy
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
                  - "*"
  ScriptResource:
    Type: AWS::GameLift::Script
    Properties:
      Name: MyRealtimeScript
      Version: v1.0
      StorageLocation:
        Bucket: "MyBucketName"
        Key: "MyScriptFiles.zip"        
        RoleArn: !GetAtt IAMRole.Arn
```

## See also<a name="aws-resource-gamelift-script--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+ [ Upload Script Files in Amazon S3](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-script-uploading.html#realtime-script-uploading-s3) in the *Amazon GameLift Developer Guide*
+  [CreateScript](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateScript.html) in the *Amazon GameLift API Reference* 