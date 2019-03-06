# AWS::RoboMaker::Robot<a name="aws-resource-robomaker-robot"></a>

The `AWS::RoboMaker::Robot` resource creates an AWS RoboMaker robot\. For more information, see [API\_CreateRobot](https://docs.aws.amazon.com/robomaker/latest/dg/API_CreateRobot) in the *RoboMaker Developer Guide*\. 

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
    "[Tags](#cfn-robomaker-robot-tags)" : JSON object
  }
}
```

### YAML<a name="aws-resource-robomaker-robot-syntax.yaml"></a>

```
Type: "AWS::RoboMaker::Robot"
Properties:
  [Architecture](#cfn-robomaker-robot-architecture): String
  [Fleet](#cfn-robomaker-robot-fleet): String
  [GreengrassGroupId](#cfn-robomaker-robot-greengrassgroupid): String
  [Name](#cfn-robomaker-robot-name): String
  [Tags](#cfn-robomaker-robot-tags): JSON object
```

## Properties<a name="aws-resource-robomaker-robot-properties"></a>

`Architecture`  <a name="cfn-robomaker-robot-architecture"></a>
The target architecture of the robot\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Fleet`  <a name="cfn-robomaker-robot-fleet"></a>
The fleet to which the robot is enlisted\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`GreengrassGroupId`  <a name="cfn-robomaker-robot-greengrassgroupid"></a>
The AWS GreenGrass group id\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-robomaker-robot-name"></a>
The name of the robot\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-robomaker-robot-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-robomaker-robot-returnvalues"></a>

### Ref<a name="aws-resource-robomaker-robot-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::Robot` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the robot, such as `arn:aws:robomaker:us-west-2:123456789012:robot/MyRobot/1544035373264`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-robomaker-robot-examples"></a>

### Create an AWS RoboMaker Robot<a name="aws-resource-robomaker-robot-example1"></a>

The following example creates a robot\.

#### JSON<a name="aws-resource-robomaker-robot-example1.json"></a>

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

#### YAML<a name="aws-resource-robomaker-robot-example1.yaml"></a>

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