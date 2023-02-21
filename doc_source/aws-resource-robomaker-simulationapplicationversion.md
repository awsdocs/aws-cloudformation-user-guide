# AWS::RoboMaker::SimulationApplicationVersion<a name="aws-resource-robomaker-simulationapplicationversion"></a>

The `AWS::RoboMaker::SimulationApplicationVersion` resource creates a version of an AWS RoboMaker simulation application\.

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
Type: AWS::RoboMaker::SimulationApplicationVersion
Properties: 
  [Application](#cfn-robomaker-simulationapplicationversion-application): String
  [CurrentRevisionId](#cfn-robomaker-simulationapplicationversion-currentrevisionid): String
```

## Properties<a name="aws-resource-robomaker-simulationapplicationversion-properties"></a>

`Application`  <a name="cfn-robomaker-simulationapplicationversion-application"></a>
The application information for the simulation application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1224`  
*Pattern*: `arn:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CurrentRevisionId`  <a name="cfn-robomaker-simulationapplicationversion-currentrevisionid"></a>
The current revision id for the simulation application\. If you provide a value and it matches the latest revision ID, a new version will be created\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `40`  
*Pattern*: `[a-zA-Z0-9_.\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-robomaker-simulationapplicationversion-return-values"></a>

### Ref<a name="aws-resource-robomaker-simulationapplicationversion-return-values-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::SimulationApplicationVersion` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the simulation application version, such as ` arn:aws:robomaker:us-west-2:123456789012:simulation-application/MySimulationApplication/1546541201334`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-robomaker-simulationapplicationversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-robomaker-simulationapplicationversion-return-values-fn--getatt-fn--getatt"></a>

`ApplicationVersion`  <a name="ApplicationVersion-fn::getatt"></a>
The simulation application version\.

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the simulation application version\.

## Examples<a name="aws-resource-robomaker-simulationapplicationversion--examples"></a>



### Create an AWS RoboMaker Simulation Application Version<a name="aws-resource-robomaker-simulationapplicationversion--examples--Create_an__RoboMaker_Simulation_Application_Version"></a>

The following example creates a simulation application version\.

#### JSON<a name="aws-resource-robomaker-simulationapplicationversion--examples--Create_an__RoboMaker_Simulation_Application_Version--json"></a>

```
{
  "Description": "RoboMaker SimulationApplicationVersion example",
  "Resources": {
    "BasicSimulationApplication": {
      "Type": "AWS::RoboMaker::SimulationApplication",
      "Properties": {
        "Name": "MySimulationApplication",
        "Environment": "111122223333.dkr.ecr.us-west-2.amazonaws.com/my-sim-app:latest",
        "RobotSoftwareSuite": {
          "Name": "General"
        },
        "SimulationSoftwareSuite": {
          "Name": "SimulationRuntime"
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

#### YAML<a name="aws-resource-robomaker-simulationapplicationversion--examples--Create_an__RoboMaker_Simulation_Application_Version--yaml"></a>

```
---
Description: "RoboMaker SimulationApplicationVersion example"
Resources:
  BasicSimulationApplication:
    Type: "AWS::RoboMaker::SimulationApplication"
    Properties:
      Name: "MySimulationApplication"
      Environment: "111122223333.dkr.ecr.us-west-2.amazonaws.com/my-sim-app:latest"
      RobotSoftwareSuite:
        Name: "General"
      SimulationSoftwareSuite:
        Name: "SimulationRuntime"
  BasicSimulationApplicationVersion:
    Type: "AWS::RoboMaker::SimulationApplicationVersion"
    Properties:
      Application: !GetAtt BasicSimulationApplication.Arn
      CurrentRevisionId: !GetAtt BasicSimulationApplication.CurrentRevisionId
Outputs:
  SimulationApplicationVersion:
    Value: !Ref BasicSimulationApplicationVersion
```