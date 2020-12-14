# AWS::RoboMaker::RobotApplication<a name="aws-resource-robomaker-robotapplication"></a>

The `AWS::RoboMaker::RobotApplication` resource creates an AWS RoboMaker robot application\.

## Syntax<a name="aws-resource-robomaker-robotapplication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-robotapplication-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::RobotApplication",
  "Properties" : {
      "[CurrentRevisionId](#cfn-robomaker-robotapplication-currentrevisionid)" : String,
      "[Name](#cfn-robomaker-robotapplication-name)" : String,
      "[RobotSoftwareSuite](#cfn-robomaker-robotapplication-robotsoftwaresuite)" : RobotSoftwareSuite,
      "[Sources](#cfn-robomaker-robotapplication-sources)" : [ SourceConfig, ... ],
      "[Tags](#cfn-robomaker-robotapplication-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-robomaker-robotapplication-syntax.yaml"></a>

```
Type: AWS::RoboMaker::RobotApplication
Properties: 
  [CurrentRevisionId](#cfn-robomaker-robotapplication-currentrevisionid): String
  [Name](#cfn-robomaker-robotapplication-name): String
  [RobotSoftwareSuite](#cfn-robomaker-robotapplication-robotsoftwaresuite): 
    RobotSoftwareSuite
  [Sources](#cfn-robomaker-robotapplication-sources): 
    - SourceConfig
  [Tags](#cfn-robomaker-robotapplication-tags): Json
```

## Properties<a name="aws-resource-robomaker-robotapplication-properties"></a>

`CurrentRevisionId`  <a name="cfn-robomaker-robotapplication-currentrevisionid"></a>
The current revision id\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-robomaker-robotapplication-name"></a>
The name of the robot application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RobotSoftwareSuite`  <a name="cfn-robomaker-robotapplication-robotsoftwaresuite"></a>
The robot software suite \(ROS distribuition\) used by the robot application\.  
*Required*: Yes  
*Type*: [RobotSoftwareSuite](aws-properties-robomaker-robotapplication-robotsoftwaresuite.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Sources`  <a name="cfn-robomaker-robotapplication-sources"></a>
The sources of the robot application\.  
*Required*: Yes  
*Type*: List of [SourceConfig](aws-properties-robomaker-robotapplication-sourceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-robomaker-robotapplication-tags"></a>
A map that contains tag keys and tag values that are attached to the robot application\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-robomaker-robotapplication-return-values"></a>

### Ref<a name="aws-resource-robomaker-robotapplication-return-values-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::RobotApplication` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the robot application, such as `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-robomaker-robotapplication-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-robomaker-robotapplication-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the robot application\.

`CurrentRevisionId`  <a name="CurrentRevisionId-fn::getatt"></a>
The current revision id\.

## Examples<a name="aws-resource-robomaker-robotapplication--examples"></a>



### Create an AWS RoboMaker Robot Application<a name="aws-resource-robomaker-robotapplication--examples--Create_an_AWS_RoboMaker_Robot_Application"></a>

The following example creates a robot application\.

#### JSON<a name="aws-resource-robomaker-robotapplication--examples--Create_an_AWS_RoboMaker_Robot_Application--json"></a>

```
{
  "Description": "Robot Application example",
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
        },
        "Tags": {
          "Name": "BasicRobotApplication",
          "Type": "CFN"
        }
      }
    }
  },
  "Outputs": {
    "RobotApplication": {
      "Value": "BasicRobotApplication"
    }
  }
}
```

#### YAML<a name="aws-resource-robomaker-robotapplication--examples--Create_an_AWS_RoboMaker_Robot_Application--yaml"></a>

```
---
Description: "Basic RobotApplication test"
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
      Tags:
        "Name" : "BasicRobotApplication"
        "Type" : "CFN"

Outputs:
  RobotApplication:
    Value: !Ref BasicRobotApplication
```