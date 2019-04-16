# AWS::RoboMaker::SimulationApplication<a name="aws-resource-robomaker-simulationapplication"></a>

The `AWS::RoboMaker::SimulationApplication` resource creates an AWS RoboMaker simulation application\. For more information, see [API\_CreateSimulationApplication](https://docs.aws.amazon.com/robomaker/latest/dg/API_CreateSimulationApplication) in the *RoboMaker Developer Guide*\. 

## Syntax<a name="aws-resource-robomaker-simulationapplication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-simulationapplication-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::SimulationApplication",
  "Properties" : {
    "[CurrentRevisionId](#cfn-robomaker-simulationapplication-currentrevisionid)" : String,
    "[Name](#cfn-robomaker-simulationapplication-name)" : String,
    "[RenderingEngine](#cfn-robomaker-simulationapplication-renderingengine)" : [*RenderingEngine*](aws-properties-robomaker-simulationapplication-renderingengine.md),
    "[RobotSoftwareSuite](#cfn-robomaker-simulationapplication-robotsoftwaresuite)" : [*RobotSoftwareSuite*](aws-properties-robomaker-simulationapplication-robotsoftwaresuite.md),
    "[SimulationSoftwareSuite](#cfn-robomaker-simulationapplication-simulationsoftwaresuite)" : [*SimulationSoftwareSuite*](aws-properties-robomaker-simulationapplication-simulationsoftwaresuite.md),
    "[Sources](#cfn-robomaker-simulationapplication-sources)" : [ [*SourceConfig*](aws-properties-robomaker-simulationapplication-sourceconfig.md), ... ],
    "[Tags](#cfn-robomaker-simulationapplication-tags)" : JSON object 
  }
}
```

### YAML<a name="aws-resource-robomaker-simulationapplication-syntax.yaml"></a>

```
Type: "AWS::RoboMaker::SimulationApplication"
Properties:
  [CurrentRevisionId](#cfn-robomaker-simulationapplication-currentrevisionid): String
  [Name](#cfn-robomaker-simulationapplication-name): String
  [RenderingEngine](#cfn-robomaker-simulationapplication-renderingengine): [*RenderingEngine*](aws-properties-robomaker-simulationapplication-renderingengine.md)
  [RobotSoftwareSuite](#cfn-robomaker-simulationapplication-robotsoftwaresuite): [*RobotSoftwareSuite*](aws-properties-robomaker-simulationapplication-robotsoftwaresuite.md)
  [SimulationSoftwareSuite](#cfn-robomaker-simulationapplication-simulationsoftwaresuite): [*SimulationSoftwareSuite*](aws-properties-robomaker-simulationapplication-simulationsoftwaresuite.md)
  [Sources](#cfn-robomaker-simulationapplication-sources): 
    - [*SourceConfig*](aws-properties-robomaker-simulationapplication-sourceconfig.md)
  [Tags](#cfn-robomaker-simulationapplication-tags): JSON object
```

## Properties<a name="aws-resource-robomaker-simulationapplication-properties"></a>

`CurrentRevisionId`  <a name="cfn-robomaker-simulationapplication-currentrevisionid"></a>
The current revision id\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-robomaker-simulationapplication-name"></a>
The name of the simulation application\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`RenderingEngine`  <a name="cfn-robomaker-simulationapplication-renderingengine"></a>
The rendering engine\.  
 *Required*: Yes  
 *Type*: [RenderingEngine](aws-properties-robomaker-simulationapplication-renderingengine.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RobotSoftwareSuite`  <a name="cfn-robomaker-simulationapplication-robotsoftwaresuite"></a>
The robot software suite\.  
 *Required*: Yes  
 *Type*: [RobotSoftwareSuite](aws-properties-robomaker-simulationapplication-robotsoftwaresuite.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SimulationSoftwareSuite`  <a name="cfn-robomaker-simulationapplication-simulationsoftwaresuite"></a>
The simulation software suite\.  
 *Required*: Yes  
 *Type*: [SimulationSoftwareSuite](aws-properties-robomaker-simulationapplication-simulationsoftwaresuite.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Sources`  <a name="cfn-robomaker-simulationapplication-sources"></a>
The sources of the simulation application\.  
 *Required*: Yes  
 *Type*: List of [SourceConfig](aws-properties-robomaker-simulationapplication-sourceconfig.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-robomaker-simulationapplication-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-robomaker-simulationapplication-returnvalues"></a>

### Ref<a name="aws-resource-robomaker-simulationapplication-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::SimulationApplication` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the simulation application, such as `arn:aws:robomaker:us-west-2:123456789012:simulation-application/MySimulationApplication/1546541201334`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-robomaker-simulationapplication-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the simulation application, such as `arn:aws:robo-maker:us-east-1:123456789012:simulation-application/simulation-application-a1bzhi`\. 

`CurrentRevisionId`  
The current revision id, such as `2`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-robomaker-simulationapplication-examples"></a>

### Create an AWS RoboMaker Simulation Application<a name="aws-resource-robomaker-simulationapplication-example1"></a>

The following example creates a simulation application\.

#### JSON<a name="aws-resource-robomaker-simulationapplication-example1.json"></a>

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

#### YAML<a name="aws-resource-robomaker-simulationapplication-example1.yaml"></a>

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