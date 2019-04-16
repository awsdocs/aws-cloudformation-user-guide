# RoboMaker SimulationApplication SimulationSoftwareSuite<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite"></a>

<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite-description"></a>The `SimulationSoftwareSuite` property type specifies the simulation software suite for an AWS RoboMaker simulation application\.

<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite-inheritance"></a> `SimulationSoftwareSuite` is a property of the [AWS::RoboMaker::SimulationApplication](aws-resource-robomaker-simulationapplication.md) resource\.

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
The simulation software suite name\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Version`  <a name="cfn-robomaker-simulationapplication-simulationsoftwaresuite-version"></a>
The simulation software suite version\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-robomaker-simulationapplication-simulationsoftwaresuite-seealso"></a>
+ [SimulationSoftwareSuite](https://docs.aws.amazon.com/robomaker/latest/dg/API_SimulationSoftwareSuite) in the *RoboMaker Developer Guide*