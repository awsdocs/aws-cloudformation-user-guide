# AWS::RoboMaker::SimulationApplicationVersion<a name="aws-resource-robomaker-simulationapplicationversion"></a>

The `AWS::RoboMaker::SimulationApplicationVersion` resource creates a version of an AWS RoboMaker simulation application\. For more information, see [API\_CreateSimulationApplicationVersion](https://docs.aws.amazon.com/robomaker/latest/dg/API_CreateSimulationApplicationVersion) in the *RoboMaker Developer Guide*\. 

## Syntax<a name="aws-resource-robomaker-simulationapplicationversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-simulationapplicationversion-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::SimulationApplicationVersion",
  "Properties" : {
    "[Application](#cfn-robomaker-simulationapplicationversion-application)" : String,
    "[CurrentRevisionId](#cfn-robomaker-simulationapplicationversion-currentrevisionid)" : String
  }
}
```

### YAML<a name="aws-resource-robomaker-simulationapplicationversion-syntax.yaml"></a>

```
Type: "AWS::RoboMaker::SimulationApplicationVersion"
Properties:
  [Application](#cfn-robomaker-simulationapplicationversion-application): String
  [CurrentRevisionId](#cfn-robomaker-simulationapplicationversion-currentrevisionid): String
```

## Properties<a name="aws-resource-robomaker-simulationapplicationversion-properties"></a>

`Application`  <a name="cfn-robomaker-simulationapplicationversion-application"></a>
The the Amazon Resource Name \(ARN\) robot application to version\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CurrentRevisionId`  <a name="cfn-robomaker-simulationapplicationversion-currentrevisionid"></a>
The current revision id\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-robomaker-simulationapplicationversion-returnvalues"></a>

### Ref<a name="aws-resource-robomaker-simulationapplicationversion-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::SimulationApplicationVersion` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the robot application, such as `arn:aws:robomaker:us-west-2:123456789012:simulation-application/MySimulationApplication/1546541201334`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-robomaker-simulationapplicationversion-examples"></a>

### Create an AWS RoboMaker Simulation Application Version<a name="aws-resource-robomaker-simulationapplicationversion-example1"></a>

The following example creates a version of a simulation application\.

#### JSON<a name="aws-resource-robomaker-simulationapplicationversion-example1.json"></a>

```
{
  "Description": "RoboMaker SimulationApplicationVersion example",
  "Resources": {
    "BasicSimulationApplication": {
      "Type": "AWS::RoboMaker::SimulationApplication",
      "Properties": {
        "Name": "MySimulationApplication",
        "Sources": [
          {
            "S3Bucket": "my-bucket",
            "S3Key": "my_simulation_bundle_x86.tar.gz",
            "Architecture": "X86_64"
          }
        ],
        "RobotSoftwareSuite": {
          "Name": "ROS",
          "Version": "Kinetic"
        },
        "SimulationSoftwareSuite": {
          "Name": "Gazebo",
          "Version": "7"
        },
        "RenderingEngine": {
          "Name": "OGRE",
          "Version": "1.x"
        }
      }
    },
    "BasicSimulationApplicationVersion": {
      "Type": "AWS::RoboMaker::SimulationApplicationVersion",
      "Properties": {
        "Application": { 
          "Fn::GetAtt" : [ "BasicSimulationApplication", "Arn" ] 
        },
        "CurrentRevisionId": { 
          "Fn::GetAtt" : [ "BasicSimulationApplication", "CurrentRevisionId" ] 
        }
      }
    }
  },
  "Outputs": {
    "SimulationApplicationVersion": {
      "Value": "BasicSimulationApplicationVersion"
    }
  }
}
```

#### YAML<a name="aws-resource-robomaker-simulationapplicationversion-example1.yaml"></a>

```
---
Description: "RoboMaker SimulationApplicationVersion example"
Resources:
  BasicSimulationApplication:
    Type: "AWS::RoboMaker::SimulationApplication"
    Properties:
      Name: "MySimulationApplication"
      Sources:
        - S3Bucket: "my-bucket"
          S3Key: "my_simulation_bundle_x86.tar.gz"
          Architecture: "X86_64"
      RobotSoftwareSuite:
        Name: "ROS"
        Version: "Kinetic"
      SimulationSoftwareSuite:
        Name: "Gazebo"
        Version: "7"
      RenderingEngine:
        Name: "OGRE"
        Version: "1.x"
  BasicSimulationApplicationVersion:
    Type: "AWS::RoboMaker::SimulationApplicationVersion"
    Properties:
      Application: !GetAtt BasicSimulationApplication.Arn
      CurrentRevisionId: !GetAtt BasicSimulationApplication.CurrentRevisionId
Outputs:
  SimulationApplicationVersion:
    Value: !Ref BasicSimulationApplicationVersion
```