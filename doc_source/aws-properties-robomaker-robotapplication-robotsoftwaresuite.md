# RoboMaker RobotApplication RobotSoftwareSuite<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite"></a>

<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite-description"></a>The `RobotSoftwareSuite` property type specifies the robotsoftware suite for an AWS RoboMaker robot application\.

<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite-inheritance"></a> `RobotSoftwareSuite` is a property of the [AWS::RoboMaker::RobotApplication](aws-resource-robomaker-robotapplication.md) resource\.

## Syntax<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite-syntax.json"></a>

```
{
  "[Name](#cfn-robomaker-robotapplication-robotsoftwaresuite-name)" : String,
  "[Version](#cfn-robomaker-robotapplication-robotsoftwaresuite-version)" : String
}
```

### YAML<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite-syntax.yaml"></a>

```
[Name](#cfn-robomaker-robotapplication-robotsoftwaresuite-name): String
[Version](#cfn-robomaker-robotapplication-robotsoftwaresuite-version): String
```

## Properties<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite-properties"></a>

`Name`  <a name="cfn-robomaker-robotapplication-robotsoftwaresuite-name"></a>
The name of the robot software suite\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Version`  <a name="cfn-robomaker-robotapplication-robotsoftwaresuite-version"></a>
The version of the robot software suite\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-robomaker-robotapplication-robotsoftwaresuite-seealso"></a>
+ [RobotSoftwareSuite](https://docs.aws.amazon.com/robomaker/latest/dg/API_RobotSoftwareSuite) in the *RoboMaker Developer Guide*