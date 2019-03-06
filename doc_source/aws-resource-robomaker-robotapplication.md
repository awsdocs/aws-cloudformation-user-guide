# AWS::RoboMaker::RobotApplication<a name="aws-resource-robomaker-robotapplication"></a>

The `AWS::RoboMaker::RobotApplication` resource creates an AWS RoboMaker robot application\. For more information, see [API\_CreateRobotApplication](https://docs.aws.amazon.com/robomaker/latest/dg/API_CreateRobotApplication) in the *RoboMaker Developer Guide*\. 

## Syntax<a name="aws-resource-robomaker-robotapplication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-robotapplication-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::RobotApplication",
  "Properties" : {
    "[CurrentRevisionId](#cfn-robomaker-robotapplication-currentrevisionid)" : String,
    "[Name](#cfn-robomaker-robotapplication-name)" : String,
    "[RobotSoftwareSuite](#cfn-robomaker-robotapplication-robotsoftwaresuite)" : [*RobotSoftwareSuite*](aws-properties-robomaker-robotapplication-robotsoftwaresuite.md),
    "[Sources](#cfn-robomaker-robotapplication-sources)" : [ [*SourceConfig*](aws-properties-robomaker-robotapplication-sourceconfig.md), ... ],
    "[Tags](#cfn-robomaker-robotapplication-tags)" : JSON object
  }
}
```

### YAML<a name="aws-resource-robomaker-robotapplication-syntax.yaml"></a>

```
Type: "AWS::RoboMaker::RobotApplication"
Properties:
  [CurrentRevisionId](#cfn-robomaker-robotapplication-currentrevisionid): String
  [Name](#cfn-robomaker-robotapplication-name): String
  [RobotSoftwareSuite](#cfn-robomaker-robotapplication-robotsoftwaresuite): 
    [*RobotSoftwareSuite*](aws-properties-robomaker-robotapplication-robotsoftwaresuite.md)
  [Sources](#cfn-robomaker-robotapplication-sources): 
    - [*SourceConfig*](aws-properties-robomaker-robotapplication-sourceconfig.md)
  [Tags](#cfn-robomaker-robotapplication-tags): JSON object
```

## Properties<a name="aws-resource-robomaker-robotapplication-properties"></a>

`CurrentRevisionId`  <a name="cfn-robomaker-robotapplication-currentrevisionid"></a>
The current revision id\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-robomaker-robotapplication-name"></a>
The name of the robot application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RobotSoftwareSuite`  <a name="cfn-robomaker-robotapplication-robotsoftwaresuite"></a>
The robot software suite\.  
 *Required*: Yes  
 *Type*: [RobotSoftwareSuite](aws-properties-robomaker-robotapplication-robotsoftwaresuite.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Sources`  <a name="cfn-robomaker-robotapplication-sources"></a>
The sources of the robot application\.  
 *Required*: Yes  
 *Type*: List of [SourceConfig](aws-properties-robomaker-robotapplication-sourceconfig.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-robomaker-robotapplication-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-robomaker-robotapplication-returnvalues"></a>

### Ref<a name="aws-resource-robomaker-robotapplication-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::RobotApplication` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the robot application, such as `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-robomaker-robotapplication-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the robot application, such as `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`\. 

`CurrentRevisionId`  
The current revision id, such as `2`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-robomaker-robotapplication-examples"></a>

### Create an AWS RoboMaker Robot Application<a name="aws-resource-robomaker-robotapplication-example1"></a>

The following example creates a robot application\.

#### JSON<a name="aws-resource-robomaker-robotapplication-example1.json"></a>

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

#### YAML<a name="aws-resource-robomaker-robotapplication-example1.yaml"></a>

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