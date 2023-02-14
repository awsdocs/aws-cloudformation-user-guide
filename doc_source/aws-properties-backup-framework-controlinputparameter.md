# AWS::Backup::Framework ControlInputParameter<a name="aws-properties-backup-framework-controlinputparameter"></a>

A list of parameters for a control\. A control can have zero, one, or more than one parameter\. An example of a control with two parameters is: "backup plan frequency is at least `daily` and the retention period is at least `1 year`"\. The first parameter is `daily`\. The second parameter is `1 year`\.

## Syntax<a name="aws-properties-backup-framework-controlinputparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-backup-framework-controlinputparameter-syntax.json"></a>

```
{
  "[ParameterName](#cfn-backup-framework-controlinputparameter-parametername)" : String,
  "[ParameterValue](#cfn-backup-framework-controlinputparameter-parametervalue)" : String
}
```

### YAML<a name="aws-properties-backup-framework-controlinputparameter-syntax.yaml"></a>

```
  [ParameterName](#cfn-backup-framework-controlinputparameter-parametername): String
  [ParameterValue](#cfn-backup-framework-controlinputparameter-parametervalue): String
```

## Properties<a name="aws-properties-backup-framework-controlinputparameter-properties"></a>

`ParameterName`  <a name="cfn-backup-framework-controlinputparameter-parametername"></a>
The name of a parameter, for example, `BackupPlanFrequency`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValue`  <a name="cfn-backup-framework-controlinputparameter-parametervalue"></a>
The value of parameter, for example, `hourly`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)