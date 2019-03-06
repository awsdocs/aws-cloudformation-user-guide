# RoboMaker SimulationApplication SourceConfig<a name="aws-properties-robomaker-simulationapplication-sourceconfig"></a>

<a name="aws-properties-robomaker-simulationapplication-sourceconfig-description"></a>The `SourceConfig` property type specifies the source configuration for an AWS RoboMaker simulation application\.

<a name="aws-properties-robomaker-simulationapplication-sourceconfig-inheritance"></a> `SourceConfig` is a property of the [AWS::RoboMaker::SimulationApplication](aws-resource-robomaker-simulationapplication.md) resource\.

## Syntax<a name="aws-properties-robomaker-simulationapplication-sourceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-robomaker-simulationapplication-sourceconfig-syntax.json"></a>

```
{
  "[Architecture](#cfn-robomaker-simulationapplication-sourceconfig-architecture)" : String,
  "[S3Bucket](#cfn-robomaker-simulationapplication-sourceconfig-s3bucket)" : String,
  "[S3Key](#cfn-robomaker-simulationapplication-sourceconfig-s3key)" : String
}
```

### YAML<a name="aws-properties-robomaker-simulationapplication-sourceconfig-syntax.yaml"></a>

```
[Architecture](#cfn-robomaker-simulationapplication-sourceconfig-architecture): String
[S3Bucket](#cfn-robomaker-simulationapplication-sourceconfig-s3bucket): String
[S3Key](#cfn-robomaker-simulationapplication-sourceconfig-s3key): String
```

## Properties<a name="aws-properties-robomaker-simulationapplication-sourceconfig-properties"></a>

`Architecture`  <a name="cfn-robomaker-simulationapplication-sourceconfig-architecture"></a>
The target processor architecture\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Bucket`  <a name="cfn-robomaker-simulationapplication-sourceconfig-s3bucket"></a>
The Amazon S3 bucket name\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Key`  <a name="cfn-robomaker-simulationapplication-sourceconfig-s3key"></a>
The Amazon S3 object key\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-robomaker-simulationapplication-sourceconfig-seealso"></a>
+ [SourceConfig](https://docs.aws.amazon.com/robomaker/latest/dg/API_SourceConfig) in the *RoboMaker Developer Guide*