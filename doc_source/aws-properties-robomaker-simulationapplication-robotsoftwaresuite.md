# AWS::RoboMaker::SimulationApplication RobotSoftwareSuite<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite"></a>

Information about a robot software suite\.

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
The name of the robot software suite\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `ROS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-robomaker-simulationapplication-robotsoftwaresuite-version"></a>
The version of the robot software suite\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `Kinetic`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-southeast-1`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
