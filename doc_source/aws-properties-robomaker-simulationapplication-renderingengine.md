# AWS::RoboMaker::SimulationApplication RenderingEngine<a name="aws-properties-robomaker-simulationapplication-renderingengine"></a>

Information about a rendering engine\.

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
  [Name](#cfn-robomaker-simulationapplication-renderingengine-name): String
  [Version](#cfn-robomaker-simulationapplication-renderingengine-version): String
```

## Properties<a name="aws-properties-robomaker-simulationapplication-renderingengine-properties"></a>

`Name`  <a name="cfn-robomaker-simulationapplication-renderingengine-name"></a>
The name of the rendering engine\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `OGRE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-robomaker-simulationapplication-renderingengine-version"></a>
The version of the rendering engine\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4`  
*Pattern*: `1.x`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)