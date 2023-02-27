# AWS::RoboMaker::RobotApplicationVersion<a name="aws-resource-robomaker-robotapplicationversion"></a>

The `AWS::RoboMaker::RobotApplicationVersion` resource creates an AWS RoboMaker robot version\.

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
Type: AWS::RoboMaker::RobotApplicationVersion
Properties: 
  [Application](#cfn-robomaker-robotapplicationversion-application): String
  [CurrentRevisionId](#cfn-robomaker-robotapplicationversion-currentrevisionid): String
```

## Properties<a name="aws-resource-robomaker-robotapplicationversion-properties"></a>

`Application`  <a name="cfn-robomaker-robotapplicationversion-application"></a>
The application information for the robot application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1224`  
*Pattern*: `arn:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CurrentRevisionId`  <a name="cfn-robomaker-robotapplicationversion-currentrevisionid"></a>
The current revision id for the robot application\. If you provide a value and it matches the latest revision ID, a new version will be created\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `40`  
*Pattern*: `[a-zA-Z0-9_.\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-robomaker-robotapplicationversion-return-values"></a>

### Ref<a name="aws-resource-robomaker-robotapplicationversion-return-values-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::RobotApplicationVersion` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the robot application version, such as `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-robomaker-robotapplicationversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-robomaker-robotapplicationversion-return-values-fn--getatt-fn--getatt"></a>

`ApplicationVersion`  <a name="ApplicationVersion-fn::getatt"></a>
The robot application version\.

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the robot application version\.

## Examples<a name="aws-resource-robomaker-robotapplicationversion--examples"></a>



### Create an AWS RoboMaker Robot Application Version<a name="aws-resource-robomaker-robotapplicationversion--examples--Create_an__RoboMaker_Robot_Application_Version"></a>

The following example creates a robot application\.

#### JSON<a name="aws-resource-robomaker-robotapplicationversion--examples--Create_an__RoboMaker_Robot_Application_Version--json"></a>

```
{
  "Description": "RoboMaker RobotApplicationVersion example",
  "Resources": {
    "BasicRobotApplication": {
      "Type": "AWS::RoboMaker::RobotApplication",
      "Properties": {
        "Name": "MyRobotApplication",
        "Environment": "111122223333.dkr.ecr.us-west-2.amazonaws.com/my-robot-app:latest",
        "RobotSoftwareSuite": {
          "Name": "General"
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

#### YAML<a name="aws-resource-robomaker-robotapplicationversion--examples--Create_an__RoboMaker_Robot_Application_Version--yaml"></a>

```
---
Description: "RoboMaker RobotApplicationVersion example"
Resources:
  BasicRobotApplication:
    Type: "AWS::RoboMaker::RobotApplication"
    Properties:
      Name: "MyRobotApplication"
      Environment: "111122223333.dkr.ecr.us-west-2.amazonaws.com/my-robot-app:latest"
      RobotSoftwareSuite:
        Name: "General"
  BasicRobotApplicationVersion:
    Type: "AWS::RoboMaker::RobotApplicationVersion"
    Properties:
      Application: !GetAtt BasicRobotApplication.Arn
      CurrentRevisionId: !GetAtt BasicRobotApplication.CurrentRevisionId
Outputs:
  RobotApplicationVersion:
    Value: !Ref BasicRobotApplicationVersion
```