# RoboMaker SimulationApplication RobotSoftwareSuite<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite"></a>

<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite-description"></a>The `RobotSoftwareSuite` property type specifies robot software suite for an AWS RoboMaker simulation application\.

<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite-inheritance"></a> `RobotSoftwareSuite` is a property of the [AWS::RoboMaker::SimulationApplication](aws-resource-robomaker-simulationapplication.md) resource\.

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
Robot software suite name\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Version`  <a name="cfn-robomaker-simulationapplication-robotsoftwaresuite-version"></a>
Robot software suite version\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-robomaker-simulationapplication-robotsoftwaresuite-seealso"></a>
+ [RobotSoftwareSuite](https://docs.aws.amazon.com/robomaker/latest/dg/API_RobotSoftwareSuite) in the *RoboMaker Developer Guide*