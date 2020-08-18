# AWS::RoboMaker::SimulationApplication SimulationSoftwareSuite<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite"></a>

Information about a simulation software suite\.

## Syntax<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite-syntax.json"></a>

```
{
  "[Name](#cfn-robomaker-simulationapplication-simulationsoftwaresuite-name)" : String,
  "[Version](#cfn-robomaker-simulationapplication-simulationsoftwaresuite-version)" : String
}
```

### YAML<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite-syntax.yaml"></a>

```
  [Name](#cfn-robomaker-simulationapplication-simulationsoftwaresuite-name): String
  [Version](#cfn-robomaker-simulationapplication-simulationsoftwaresuite-version): String
```

## Properties<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite-properties"></a>

`Name`  <a name="cfn-robomaker-simulationapplication-simulationsoftwaresuite-name"></a>
The name of the simulation software suite\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Gazebo | RosbagPlay`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-robomaker-simulationapplication-simulationsoftwaresuite-version"></a>
The version of the simulation software suite\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `7|9|Kinetic|Melodic|Dashing`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)