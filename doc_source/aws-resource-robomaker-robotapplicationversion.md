# AWS::RoboMaker::RobotApplicationVersion<a name="aws-resource-robomaker-robotapplicationversion"></a>

The `AWS::RoboMaker::RobotApplicationVersion` resource creates a version of an AWS RoboMaker robot application\. For more information, see [API\_CreateRobotApplicationVersion](https://docs.aws.amazon.com/robomaker/latest/dg/API_CreateRobotApplicationVersion) in the *RoboMaker Developer Guide*\. 

## Syntax<a name="aws-resource-robomaker-robotapplicationversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-robotapplicationversion-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::RobotApplicationVersion",
  "Properties" : {
    "[Application](#cfn-robomaker-robotapplicationversion-application)" : String,
    "[CurrentRevisionId](#cfn-robomaker-robotapplicationversion-currentrevisionid)" : String
  }
}
```

### YAML<a name="aws-resource-robomaker-robotapplicationversion-syntax.yaml"></a>

```
Type: "AWS::RoboMaker::RobotApplicationVersion"
Properties:
  [Application](#cfn-robomaker-robotapplicationversion-application): String
  [CurrentRevisionId](#cfn-robomaker-robotapplicationversion-currentrevisionid): String
```

## Properties<a name="aws-resource-robomaker-robotapplicationversion-properties"></a>

`Application`  <a name="cfn-robomaker-robotapplicationversion-application"></a>
The the Amazon Resource Name \(ARN\) robot application to version\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CurrentRevisionId`  <a name="cfn-robomaker-robotapplicationversion-currentrevisionid"></a>
Current revision id\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-robomaker-robotapplicationversion-returnvalues"></a>

### Ref<a name="aws-resource-robomaker-robotapplicationversion-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::RobotApplicationVersion` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the robot application, such as `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-robomaker-robotapplicationversion-examples"></a>

### Create an AWS RoboMaker Robot Application Version<a name="aws-resource-robomaker-robotapplicationversion-example1"></a>

The following example creates a version of a robot application\.

#### JSON<a name="aws-resource-robomaker-robotapplicationversion-example1.json"></a>

```
{
  "Description": "RoboMaker RobotApplicationVersion example",
  "Resources": {
    "BasicRobotApplication": {
      "Type": "AWS::RoboMaker::RobotApplication",
      "Properties": {
        "Name": "MyRobotApplication",
        "Sources": [
          {
            "S3Bucket": "my-bucket",
            "S3Key": "robot_bundle_x86.tar.gz",
            "Architecture": "ARMHF"
          }
        ],
        "RobotSoftwareSuite": {
          "Name": "ROS",
          "Version": "Kinetic"
        }
      }
    },
    "BasicRobotApplicationVersion": {
      "Type": "AWS::RoboMaker::RobotApplicationVersion",
      "Properties": {
        "Application": { 
          "Fn::GetAtt" : [ "BasicRobotApplication", "Arn" ] 
        },
        "CurrentRevisionId": { 
          "Fn::GetAtt" : [ "BasicRobotApplication", "CurrentRevisionId" ] 
        }
      }
    }
  },
  "Outputs": {
    "RobotApplicationVersion": {
      "Value": "BasicRobotApplicationVersion"
    }
  }
}
```

#### YAML<a name="aws-resource-robomaker-robotapplicationversion-example1.yaml"></a>

```
---
Description: "RoboMaker RobotApplicationVersion example"
Resources:
  BasicRobotApplication:
    Type: "AWS::RoboMaker::RobotApplication"
    Properties:
      Name: "MyRobotApplication"
      Sources:
        - S3Bucket: "my-bucket"
          S3Key: "robot_bundle_x86.tar.gz"
          Architecture: "ARMHF"
      RobotSoftwareSuite:
        Name: "ROS"
        Version: "Kinetic"
  BasicRobotApplicationVersion:
    Type: "AWS::RoboMaker::RobotApplicationVersion"
    Properties:
      Application: !GetAtt BasicRobotApplication.Arn
      CurrentRevisionId: !GetAtt BasicRobotApplication.CurrentRevisionId
Outputs:
  RobotApplicationVersion:
    Value: !Ref BasicRobotApplicationVersion
```