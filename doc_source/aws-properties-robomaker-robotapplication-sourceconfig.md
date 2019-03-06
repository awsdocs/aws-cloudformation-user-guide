# RoboMaker RobotApplication SourceConfig<a name="aws-properties-robomaker-robotapplication-sourceconfig"></a>

<a name="aws-properties-robomaker-robotapplication-sourceconfig-description"></a>The `SourceConfig` property type specifies the source configuration for an AWS RoboMaker robot application\.

<a name="aws-properties-robomaker-robotapplication-sourceconfig-inheritance"></a> `SourceConfig` is a property of the [AWS::RoboMaker::RobotApplication](aws-resource-robomaker-robotapplication.md) resource\.

## Syntax<a name="aws-properties-robomaker-robotapplication-sourceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-robomaker-robotapplication-sourceconfig-syntax.json"></a>

```
{
  "[Architecture](#cfn-robomaker-robotapplication-sourceconfig-architecture)" : String,
  "[S3Bucket](#cfn-robomaker-robotapplication-sourceconfig-s3bucket)" : String,
  "[S3Key](#cfn-robomaker-robotapplication-sourceconfig-s3key)" : String
}
```

### YAML<a name="aws-properties-robomaker-robotapplication-sourceconfig-syntax.yaml"></a>

```
[Architecture](#cfn-robomaker-robotapplication-sourceconfig-architecture): String
[S3Bucket](#cfn-robomaker-robotapplication-sourceconfig-s3bucket): String
[S3Key](#cfn-robomaker-robotapplication-sourceconfig-s3key): String
```

## Properties<a name="aws-properties-robomaker-robotapplication-sourceconfig-properties"></a>

`Architecture`  <a name="cfn-robomaker-robotapplication-sourceconfig-architecture"></a>
The target processor architecture for the application\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Bucket`  <a name="cfn-robomaker-robotapplication-sourceconfig-s3bucket"></a>
Amazon S3 bucket name\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`S3Key`  <a name="cfn-robomaker-robotapplication-sourceconfig-s3key"></a>
The Amazon S3 object key\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-robomaker-robotapplication-sourceconfig-seealso"></a>
+ [SourceConfig](https://docs.aws.amazon.com/robomaker/latest/dg/API_SourceConfig) in the *RoboMaker Developer Guide*