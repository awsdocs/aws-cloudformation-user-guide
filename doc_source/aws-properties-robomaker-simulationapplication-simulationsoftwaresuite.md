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
*Allowed Values*: `Gazebo`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-robomaker-simulationapplication-simulationsoftwaresuite-version"></a>
The version of the simulation software suite\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `7|9`  
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
