# AWS::RoboMaker::Robot<a name="aws-resource-robomaker-robot"></a>

**Important**  
The following resource is now deprecated\. This resource can no longer be provisioned via stack create or update operations, and should not be included in your stack templates\.  
  
We recommend migrating to AWS IoT Greengrass Version 2\. For more information, see [Support Changes: May 2, 2022](https://docs.aws.amazon.com/robomaker/latest/dg/chapter-support-policy.html#software-support-policy-may2022) in the *AWS RoboMaker Developer Guide*\.

The `AWS::RoboMaker::RobotApplication` resource creates an AWS RoboMaker robot\.

## Syntax<a name="aws-resource-robomaker-robot-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-robot-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::Robot",
  "Properties" : {
      "[Architecture](#cfn-robomaker-robot-architecture)" : String,
      "[Fleet](#cfn-robomaker-robot-fleet)" : String,
      "[GreengrassGroupId](#cfn-robomaker-robot-greengrassgroupid)" : String,
      "[Name](#cfn-robomaker-robot-name)" : String,
      "[Tags](#cfn-robomaker-robot-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-robomaker-robot-syntax.yaml"></a>

```
Type: AWS::RoboMaker::Robot
Properties: 
  [Architecture](#cfn-robomaker-robot-architecture): String
  [Fleet](#cfn-robomaker-robot-fleet): String
  [GreengrassGroupId](#cfn-robomaker-robot-greengrassgroupid): String
  [Name](#cfn-robomaker-robot-name): String
  [Tags](#cfn-robomaker-robot-tags): 
    Key : Value
```

## Properties<a name="aws-resource-robomaker-robot-properties"></a>

`Architecture`  <a name="cfn-robomaker-robot-architecture"></a>
The architecture of the robot\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ARM64 | ARMHF | X86_64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Fleet`  <a name="cfn-robomaker-robot-fleet"></a>
The Amazon Resource Name \(ARN\) of the fleet to which the robot will be registered\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GreengrassGroupId`  <a name="cfn-robomaker-robot-greengrassgroupid"></a>
The Greengrass group associated with the robot\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1224`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-robomaker-robot-name"></a>
The name of the robot\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-robomaker-robot-tags"></a>
A map that contains tag keys and tag values that are attached to the robot\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-robomaker-robot-return-values"></a>

### Ref<a name="aws-resource-robomaker-robot-return-values-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::Robot` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the robot application, such as `arn:aws:robomaker:us-west-2:123456789012:robot/MyRobot/1544035373264`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-robomaker-robot-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-robomaker-robot-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the robot\.

## Examples<a name="aws-resource-robomaker-robot--examples"></a>



### Create an AWS RoboMaker Robot<a name="aws-resource-robomaker-robot--examples--Create_an__RoboMaker_Robot"></a>

The following example creates a robot\.

#### JSON<a name="aws-resource-robomaker-robot--examples--Create_an__RoboMaker_Robot--json"></a>

```
{
  "Description": "RoboMaker Robot example",
  "Resources": {
    "BasicFleet": {
      "Type": "AWS::RoboMaker::Fleet",
      "Properties": {
        "Name": "MyFleet"
      }
    },
    "BasicRobot": {
      "Type": "AWS::RoboMaker::Robot",
      "Properties": {
        "Name": "MyRobot",
        "GreengrassGroupId": "51229986-abdc-4ca6-94f8-04735a0c9f07",
        "Architecture": "ARMHF",
        "Fleet": { 
          "Fn::GetAtt" : [ "BasicFleet", "Arn" ] 
        },
        "Tags": {
          "Name": "BasicRobot",
          "Type": "CFN"
        }
      }
    }
  },
  "Outputs": {
    "Robot": {
      "Value": "BasicRobot"
    }
  }
}
```

#### YAML<a name="aws-resource-robomaker-robot--examples--Create_an__RoboMaker_Robot--yaml"></a>

```
---
Description: "RoboMaker Robot example"
Resources:
  BasicFleet:
    Type: "AWS::RoboMaker::Fleet"
    Properties:
      Name: "MyFleet"
  BasicRobot:
    Type: "AWS::RoboMaker::Robot"
    Properties:
      Name: "MyRobot"
      GreengrassGroupId: "51229986-abdc-4ca6-94f8-04735a0c9f07"
      Architecture: "ARMHF"
      Fleet: !GetAtt BasicFleet.Arn
      Tags:
        "Name" : "BasicRobot"
        "Type" : "CFN"
Outputs:
  Robot:
    Value: !Ref BasicRobot
```