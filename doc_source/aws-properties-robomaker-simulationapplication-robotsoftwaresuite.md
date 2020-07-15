# AWS::RoboMaker::SimulationApplication RobotSoftwareSuite<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite"></a>

Information about a robot software suite \(ROS distribution\)\.

## Syntax<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite-syntax.json"></a>

```
{
  "[Name](#cfn-robomaker-simulationapplication-robotsoftwaresuite-name)" : String,
  "[Version](#cfn-robomaker-simulationapplication-robotsoftwaresuite-version)" : String
}
```

### YAML<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite-syntax.yaml"></a>

```
  [Name](#cfn-robomaker-simulationapplication-robotsoftwaresuite-name): String
  [Version](#cfn-robomaker-simulationapplication-robotsoftwaresuite-version): String
```

## Properties<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite-properties"></a>

`Name`  <a name="cfn-robomaker-simulationapplication-robotsoftwaresuite-name"></a>
The name of the robot software suite \(ROS distribution\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ROS | ROS2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-robomaker-simulationapplication-robotsoftwaresuite-version"></a>
The version of the robot software suite \(ROS distribution\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Dashing | Kinetic | Melodic`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)