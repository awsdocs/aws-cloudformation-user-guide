# AWS::RoboMaker::SimulationApplication SourceConfig<a name="aws-properties-robomaker-simulationapplication-sourceconfig"></a>

Information about a source configuration\.

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
The target processor architecture for the application\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ARM64 | ARMHF | X86_64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Bucket`  <a name="cfn-robomaker-simulationapplication-sourceconfig-s3bucket"></a>
The Amazon S3 bucket name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-z0-9][a-z0-9.\-]*[a-z0-9]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Key`  <a name="cfn-robomaker-simulationapplication-sourceconfig-s3key"></a>
The s3 object key\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)