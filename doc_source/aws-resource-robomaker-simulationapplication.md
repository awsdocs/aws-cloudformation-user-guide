# AWS::RoboMaker::SimulationApplication<a name="aws-resource-robomaker-simulationapplication"></a>

The `AWS::RoboMaker::SimulationApplication` resource creates an AWS RoboMaker simulation application\.

## Syntax<a name="aws-resource-robomaker-simulationapplication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-simulationapplication-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::SimulationApplication",
  "Properties" : {
      "[CurrentRevisionId](#cfn-robomaker-simulationapplication-currentrevisionid)" : String,
      "[Name](#cfn-robomaker-simulationapplication-name)" : String,
      "[RenderingEngine](#cfn-robomaker-simulationapplication-renderingengine)" : RenderingEngine,
      "[RobotSoftwareSuite](#cfn-robomaker-simulationapplication-robotsoftwaresuite)" : RobotSoftwareSuite,
      "[SimulationSoftwareSuite](#cfn-robomaker-simulationapplication-simulationsoftwaresuite)" : SimulationSoftwareSuite,
      "[Sources](#cfn-robomaker-simulationapplication-sources)" : [ SourceConfig, ... ],
      "[Tags](#cfn-robomaker-simulationapplication-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-robomaker-simulationapplication-syntax.yaml"></a>

```
Type: AWS::RoboMaker::SimulationApplication
Properties: 
  [CurrentRevisionId](#cfn-robomaker-simulationapplication-currentrevisionid): String
  [Name](#cfn-robomaker-simulationapplication-name): String
  [RenderingEngine](#cfn-robomaker-simulationapplication-renderingengine): 
    RenderingEngine
  [RobotSoftwareSuite](#cfn-robomaker-simulationapplication-robotsoftwaresuite): 
    RobotSoftwareSuite
  [SimulationSoftwareSuite](#cfn-robomaker-simulationapplication-simulationsoftwaresuite): 
    SimulationSoftwareSuite
  [Sources](#cfn-robomaker-simulationapplication-sources): 
    - SourceConfig
  [Tags](#cfn-robomaker-simulationapplication-tags): Json
```

## Properties<a name="aws-resource-robomaker-simulationapplication-properties"></a>

`CurrentRevisionId`  <a name="cfn-robomaker-simulationapplication-currentrevisionid"></a>
The current revision id\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-robomaker-simulationapplication-name"></a>
The name of the simulation application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RenderingEngine`  <a name="cfn-robomaker-simulationapplication-renderingengine"></a>
The rendering engine for the simulation application\.  
*Required*: Yes  
*Type*: [RenderingEngine](aws-properties-robomaker-simulationapplication-renderingengine.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RobotSoftwareSuite`  <a name="cfn-robomaker-simulationapplication-robotsoftwaresuite"></a>
The robot software suite \(ROS distribution\) used by the simulation application\.  
*Required*: Yes  
*Type*: [RobotSoftwareSuite](aws-properties-robomaker-simulationapplication-robotsoftwaresuite.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SimulationSoftwareSuite`  <a name="cfn-robomaker-simulationapplication-simulationsoftwaresuite"></a>
The simulation software suite used by the simulation application\.  
*Required*: Yes  
*Type*: [SimulationSoftwareSuite](aws-properties-robomaker-simulationapplication-simulationsoftwaresuite.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Sources`  <a name="cfn-robomaker-simulationapplication-sources"></a>
The sources of the simulation application\.  
*Required*: Yes  
*Type*: List of [SourceConfig](aws-properties-robomaker-simulationapplication-sourceconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-robomaker-simulationapplication-tags"></a>
A map that contains tag keys and tag values that are attached to the simulation application\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-robomaker-simulationapplication-return-values"></a>

### Ref<a name="aws-resource-robomaker-simulationapplication-return-values-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::SimulationApplication` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the simulation application, such as `arn:aws:robomaker:us-west-2:123456789012:simulation-application/MySimulationApplication/1546541201334`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-robomaker-simulationapplication-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-robomaker-simulationapplication-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the simulation application\.

`CurrentRevisionId`  <a name="CurrentRevisionId-fn::getatt"></a>
The current revision id\.

## Examples<a name="aws-resource-robomaker-simulationapplication--examples"></a>



### Create an AWS RoboMaker Simulation Application<a name="aws-resource-robomaker-simulationapplication--examples--Create_an_AWS_RoboMaker_Simulation_Application"></a>

The following example creates a simulation application\.

#### JSON<a name="aws-resource-robomaker-simulationapplication--examples--Create_an_AWS_RoboMaker_Simulation_Application--json"></a>

```
{
  "Description": "RoboMaker SimulationApplication example",
  "Resources": {
    "BasicSimulationApplication": {
      "Type": "AWS::RoboMaker::SimulationApplication",
      "Properties": {
        "Name": "MySimulationApplication",
        "Sources": [
          {
            "S3Bucket": "my-bucket",
            "S3Key": "robot_bundle_x86.tar.gz",
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
        },
        "Tags": {
          "Name": "BasicSimulationApplication",
          "Type": "CFN"
        }
      }
    }
  },
  "Outputs": {
    "SimulationApplication": {
      "Value": "BasicSimulationApplication"
    }
  }
}
```

#### YAML<a name="aws-resource-robomaker-simulationapplication--examples--Create_an_AWS_RoboMaker_Simulation_Application--yaml"></a>

```
---
Description: "RoboMaker SimulationApplication example"
Resources:
  BasicSimulationApplication:
    Type: "AWS::RoboMaker::SimulationApplication"
    Properties:
      Name: "MySimulationApplication"
      Sources:
        - S3Bucket: "my-bucket"
          S3Key: "robot_bundle_x86.tar.gz"
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
      Tags:
        "Name" : "BasicSimulationApplication"
        "Type" : "CFN"
Outputs:
  SimulationApplication:
    Value: !Ref BasicSimulationApplication
```