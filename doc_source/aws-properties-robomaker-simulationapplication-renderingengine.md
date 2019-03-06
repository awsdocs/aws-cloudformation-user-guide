# RoboMaker SimulationApplication RenderingEngine<a name="aws-properties-robomaker-simulationapplication-renderingengine"></a>

<a name="aws-properties-robomaker-simulationapplication-renderingengine-description"></a>The `RenderingEngine` property type specifies the rendering engine for an AWS RoboMaker simulation application\.

<a name="aws-properties-robomaker-simulationapplication-renderingengine-inheritance"></a> `RenderingEngine` is a property of the [AWS::RoboMaker::SimulationApplication](aws-resource-robomaker-simulationapplication.md) resource\.

## Syntax<a name="aws-properties-robomaker-simulationapplication-renderingengine-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-robomaker-simulationapplication-renderingengine-syntax.json"></a>

```
{
  "[Name](#cfn-robomaker-simulationapplication-renderingengine-name)" : String,
  "[Version](#cfn-robomaker-simulationapplication-renderingengine-version)" : String
}
```

### YAML<a name="aws-properties-robomaker-simulationapplication-renderingengine-syntax.yaml"></a>

```
[Name](#cfn-robomaker-simulationapplication-renderingengine-name) : String,
[Version](#cfn-robomaker-simulationapplication-renderingengine-version): String
```

## Properties<a name="aws-properties-robomaker-simulationapplication-renderingengine-properties"></a>

`Name`  <a name="cfn-robomaker-simulationapplication-renderingengine-name"></a>
The name of the rendering engine\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Version`  <a name="cfn-robomaker-simulationapplication-renderingengine-version"></a>
The version of the rendering engine\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-robomaker-simulationapplication-renderingengine-seealso"></a>
+ [RenderingEngine](https://docs.aws.amazon.com/robomaker/latest/dg/API_RenderingEngine) in the *RoboMaker Developer Guide*